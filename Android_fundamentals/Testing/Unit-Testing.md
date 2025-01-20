Testing smallest unit of code in isolation. The main motive of unit testing the segregation of the code into Pure Kotlin/Java and Android Framework code and testing it in isolation.

Types of Unit Test:
1. **JVM Tests**: Pure Kotlin code can be tested with JVM using. (Local Unit Test)
2. **Instrumentation tests**: On device tests
	1. UI Test: There has to be interaction with views. (Espresso)
	2. Non-UI Test: Context, Asset manager, etc.


#### Local Unit Test

In android for running local unit tests we use JUnit framework. Annotations are used to mark the functions that will used to evaluate the actual code.

1. @Test
   This is used to say that the function under this is used to test a code unit.
   Here we generally carryout the task in 3 steps
	   1. Arrange: Do the initial setup
	   2. Act: Call the required code that needs testing
	   3. Assert: Verify that the input and output is as expected

2. @Before
   This is used to say that the function under this executed before every test
   
3. @After
   This is used to say that the function under this executed after every test
   
4. @Parameterized.Parmeters(name= "Name")
   This is used to say that the function under this will provide the parameters for testing.
   The class that uses this will have be annotated with 
   @RunWith(value = Parameterized::Class)

