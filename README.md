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
```kotlin
 val filteredName = std.filter { it -> it.name.startsWith('s') }.map { s -> s.name }
        for (t in filteredName) println("SUP $t") //Output:- supriya saurabh
```
## predicate in kotlin:- all | any | count | find
```kotlin
//Given List
 val dataList = listOf<Int>(1, 4, 11,31, 21, 6, 8, 9)
```
## all
```kotlin
var resultData = dataList.all { it > 5 } // return boolean value
 println(resultData) //output :- false (because all elements are not grater than 5)
```
## any
```kotlin
 resultData = dataList.any { it > 5 } // return boolean value
 println(resultData) //output :- true (because any one or more item are grater than 5)
```
## count
```kotlin
  var countNum = dataList.count { it < 10 } // return total count Integer value
  println(countNum) // output:- 5 {1,4,6,8,9 are smaller then 10 so total count will be 5}
```
## find
```kotlin
 var foundNum = dataList.find { it > 7 } // returns first greater than 7 number from the list
 println(foundNum) // output:- 8
```



