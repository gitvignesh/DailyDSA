Solution:
https://leetcode.com/problems/best-time-to-buy-and-sell-stock/submissions/1285608083

```kotlin
fun maxProfit(prices: IntArray): Int {
	var curProfit = 0
	var maxProfit = 0
	var buy = prices[0]

	for(i in 1..prices.size-1){
		val sell = prices[i]
		if(sell>buy){
			curProfit = sell-buy
			maxProfit = max(curProfit, maxProfit)
		} else {
			buy = sell
		}
	}

	return maxProfit
}
```