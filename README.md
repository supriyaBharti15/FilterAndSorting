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

