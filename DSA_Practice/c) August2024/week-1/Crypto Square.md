Implement the classic method for composing secret messages called a square code.

Given an English text, output the encoded version of that text.

First, the input is normalized: the spaces and punctuation are removed from the English text and the message is down-cased.

Then, the normalized characters are broken into rows. These rows can be regarded as forming a rectangle when printed with intervening newlines.

Solution:
```kotlin
object CryptoSquare {

    fun ciphertext(plaintext: String): String {
        val data = plaintext.toList()
            .filter {
                it.isLetterOrDigit()
            }.map {
                it.lowercaseChar().toString()
            } as MutableList<String>
        
        val rowCol = getRowAndCol(data.size)

        while (data.size != rowCol.first * rowCol.second) {
            data.add(" ")
        }
        
        var result = MutableList<String> (rowCol.first * rowCol.second) {""}

        for (i in data.indices) {
            val row = i/rowCol.second
            val offset = i % rowCol.second
            val index = offset * rowCol.first + row
            result[index] = data[i]
        }


        return if (result.size > 0) {
            val rows = result.chunked(rowCol.first) {
                it.joinToString("")
            }
            rows.joinToString(" ")
        } else {
            ""
        }
    }

    private fun getRowAndCol(totalChars: Int): Pair<Int, Int> {
        var row = 0
        var col = 0

        while (row * col < totalChars) {
            if (col - row < 1) {
                col++
            } else {
                row++
            }
        }

        return Pair(row, col)
    }
}
```