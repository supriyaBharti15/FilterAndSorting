# FilterAndSorting
Filter | Map | FlatMap  in Kotlin
## filter
- Transforms collection.
- Filter unwanted code.
- Similar as 'where' in SQL.
```kotlin
val list = listOf(13, 21, 3, 24, 55, 63, 77)

        //Find Smallest item in the list
        val smallNum = list.filter { it < 25 }
        for (i in smallNum) println("SUP $i")
```
## map
- Transforms items.
- Similar to 'select' in SQL
```kotlin
// find square of elements
   val squareNum = list.map { it*it }
   for (i in squareNum) println("SUP $i")
```
## map and filter both example
```kotlin
//find square and filter both
  val squareFilter = list.map { it * it }.filter { it <30 }
  for (i in squareFilter) println("SUP $i")
```
## map with class | how to use map to get data from class and do operation on that
```kotlin
//Class on which we will use map 
 class Student(var name: String, var rollNo: Int) {}
```
```kotlin
//1. operation
 val std = listOf(Student("supriya", 12), Student("navin", 23), Student("Saurabh", 11))
        val name = std.map { s-> s.name }
        println("SUP $name") //Output :- [supriya, navin, Saurabh]
         for(t in name) println("SUP $t") // Output:- supriya navin  Saurabh
```


