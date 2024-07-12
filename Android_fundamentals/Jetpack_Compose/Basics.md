Jetpack compose is a native UI tool kit written in kotlin, It is packaged as a library and not a part of the framework. Basic building block is a Composable  (Kotlin function with @Composable )

```kotlin
@Composable
fun HelloCompose(name: String) {
	Text(text = "hi $name")
}
```

XML was a imperative framework whereas Jetpack Compose is a declarative framework, it based on the ideology of compose over inheritance.

### Points to Note
1. Recomposition: Whenever the state of the app changes the UI is recreated.
2. The main compose activity is inherited from component activity as it has various features that would help us handle the lifecycle components as it is lifecycle aware. while using XML we used to inherit from AppCompact activity to have backward compatibility with material design components, Action bar support, Fragment management etc.
3. To use compose along with the XML based project we use ComposeView in the layout that requires the view.
 ```xml
 <Parent>
 <ComposeView
	....
	....
	.... />
 </Parent>
  ```
4. 

### Basic Composables:

***Text***
Used to show text on screen
```kotlin
Text(
text = "", {REQUIRED}
fontStyle = FontStyle.Italic | FontStyle.Normal,
fontWeight = FontWeight.Bold | .... ,
color = Color.Red | ...... ,
fontSize = 36.sp 
textAlign = TextAlign.Centre | ..... ,
)
```

***Image***
used to show image on screen 
```kotlin
Image(
painter = painterResource(id = R.id.image1), {REQUIRED}
contentDescription = "", {REQUIRED}
colorFilter = ColourFilter.tint(Color.Blue),
contentScale = ContentScale.Crop | ..... ,
)
```

***Button***
used to show button using other Composables function
```kotlin
Button(
onClick = { /*lambda function to handle click*/ }, {REQUIRED}
colors = ButtonDefaults.buttonColors(),
enabled = true | false,
) {
Composable() //Accepts a composable in rowscope
}
```

***Text Field***
used to get text input from the user
```kotlin
TextField(
value = " ",{REQUIRED}
onValueChange = { },{REQUIRED}
lable = { Composable() },
placeHolder = { Composable() }
)
```
### Basic Layouts:

***Box***
```kotlin
Box(
contentAligment = Alignment.BottomEnd
) {
Composables()
}
```

***Column***

```kotlin
Column(
verticalArrangement = Arrangement.SpaceEvenly,
horizontalAligment = Alignment.CentreHorizonatally,

) {
Composables()
}
```


***Row***

```kotlin
Row(
horizontalArrangement = Arrangement.SpaceEvenly,
verticalAligment = Alignment.CentreVertically,

) {
Composables()
}
```

### Basic Decorators:

