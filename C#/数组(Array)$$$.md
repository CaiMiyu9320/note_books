# 数组（Array）

数组是一个存储相同类型元素的固定大小的顺序集合。数组是用来存储数据的集合，通常认为数组是一个同一类型变量的集合。

声明数组变量并不是声明 number0、number1、...、number99 一个个单独的变量，而是声明一个就像 numbers 这样的变量，然后使用 numbers[0]、numbers[1]、...、numbers[99] 来表示一个个单独的变量。数组中某个指定的元素是通过索引来访问的。

所有的数组都是由连续的内存位置组成的。最低的地址对应第一个元素，最高的地址对应最后一个元素。

## 声明数组

```C#
datatype[] arrayName;
```

> + datatype 用于指定被存储在数组中的元素的类型。
> 
> + 指定数组的秩（维度）。秩指定数组的大小。
> 
> + arrayName 指定数组的名称。

如: `double[] balance;`

## 初始化数组

声明一个数组不会在内存中初始化数组。当初始化数组变量时，您可以赋值给数组。
数组是一个引用类型，所以您需要使用 new 关键字来创建数组的实例。
如: `double[] balance = new double[10];`

## 赋值给数组

可以通过使用索引号赋值给一个单独的数组元素，比如：

```C#
double[] balance = new double[10];
balance[0] = 4500.0;
```

可以在声明数组的同时给数组赋值，比如：`double[] balance = { 2340.0, 4523.69, 3421.0};`
也可以创建并初始化一个数组，比如：`int [] marks = new int[5]  { 99,  98, 92, 97, 95};`
在上述情况下，你也可以省略数组的大小，比如：`int [] marks = new int[]  { 99,  98, 92, 97, 95};`
您也可以赋值一个数组变量到另一个目标数组变量中。在这种情况下，目标和源会指向相同的内存位置：

```C#
int [] marks = new int[]  { 99,  98, 92, 97, 95};
int[] score = marks;
```
## 访问数组元素
元素是通过带索引的数组名称来访问的。这是通过把元素的索引放置在数组名称后的方括号中来实现的。例如：
```C#
double salary = balance[9];
```
实例
```C#
using System;
namespace ArrayApplication
{
   class MyArray
   {
      static void Main(string[] args)
      {
         int []  n = new int[10]; /* n 是一个带有 10 个整数的数组 */
         int i,j;


         /* 初始化数组 n 中的元素 */         
         for ( i = 0; i < 10; i++ )
         {
            n[ i ] = i + 100;
         }

         /* 输出每个数组元素的值 */
         for (j = 0; j < 10; j++ )
         {
            Console.WriteLine("Element[{0}] = {1}", j, n[j]);
         }
         Console.ReadKey();
      }
   }
}
```

## 使用 foreach 循环
在前面的实例中，我们使用一个 for 循环来访问每个数组元素，您也可以使用一个 foreach 语句来遍历数组。

以下实例我们使用 foreach 来遍历一个数组：
```C#
using System;

namespace ArrayApplication
{
   class MyArray
   {
      static void Main(string[] args)
      {
         int []  n = new int[10]; /* n 是一个带有 10 个整数的数组 */


         /* 初始化数组 n 中的元素 */         
         for ( int i = 0; i < 10; i++ )
         {
            n[i] = i + 100;
         }

         /* 输出每个数组元素的值 */
         foreach (int j in n )
         {
            int i = j-100;
            Console.WriteLine("Element[{0}] = {1}", i, j);
         }
         Console.ReadKey();
      }
   }
}
```

## 数组细节
