# Python Convert String to Int – How to Cast a String in Python

When you're programming, you'll often need to switch between data types.
The ability to convert one data type to another gives you great flexibility when working with information.
There are different built-in ways to convert, or cast, types in the Python programming language.
In this article, you'll learn how to convert a string to an integer.
Let's get started!

プログラミングを行っている時、データの型の変換が必要となることがあるでしょう。
あるデータの型を他のデータの型に変換する知識は、情報と機能するときに、プログラマーにとって、素晴らしい柔軟性をもたらします。
Pythonというプログラミング言語において、型を変換、もしくは、キャストする方法が異なります。
この記事では、String型をInt型に変換する方法について、学べます。
それでは、詳しく見てきましょう。

## Data types in Python
Python supports a variety of data types.
Data types are used for specifying, representing, and categorizing the different kinds of data that exist and are used in computer programs.
Also, different operations are available with different types of data – one operation available in one data type is often not available in another.

One example of a data type is strings.
Strings are sequences of characters that are used for conveying textual information.
They are enclosed in single or double quotation marks, like so:

Pythonは、様々なデータの型をサポートしています。
データの型は、コンピュータのプログラムで使われている、そして、存在している異なるタイプのデータの型を特定、再表示、区別するのに使われています。
また、違う実行システムは、異なるデータの型を利用できます。つまり、あるデータの型で実行できることは、他ではよく利用できません。

データの型の一例として、String型があります。
文字は、テキストベースの情報を扱うのに使われている文字列となります。
文字は、以下のコードのように、シングル、あるいは、ダブルクォテーションで囲われます。

Ints, or integers, are whole numbers.
They are used to represent numerical data, and you can do any mathematical operation (such as addition, subtraction, multiplication, and division) when working with integers.
Integers are not enclosed in single or double quotation marks.

Int型や数字は、数字全体です。
それらは、数値データを表すのに使われます。そして、数字を用いるとき、＋、ー、✖︎、÷といった四則演算で使うことができます。
整数は、シングル、あるいはダブルクオテーションで囲われません。


## Data type conversion
Sometimes when you're storing data, or when you receive input from a user in one type, you'll need to manipulate and perform different kinds of operations on that data.
Since each data type can be manipulated in different ways, this often means that you'll need to convert it.
Converting one data type to another is also called type casting or type conversion. Many languages offer built-in cast operators to do just that – to explicitly convert one type to another.

データを保存するとき、あるいは、ユーザーから入力された型データを受け取るとき、そのデータにさまざまな操作を行うこともあるでしょう。
それぞれの型データは、異なる方法で、操作され、このことは、データの型を変更する必要があるということを意味しています。
あるデータの型を他のデータの型へ変換することを型変換あるいはキャストとも言われています。たくさんのプログラミング言語では、ある型から他の型への変換を組み込みの型変換機能として、提供しています。


## How to convert a string to an integer in Python
To convert, or cast, a string to an integer in Python, you use the int() built-in function.
The function takes in as a parameter the initial string you want to convert, and returns the integer equivalent of the value you passed.
The general syntax looks something like this: int("str").
Let's take the following example, where there is the string version of a number:



```
#string version of the number 7
print("7")

#check the data type with type() method
print(type("7"))

#output

#7
#<class 'str'>
```
To convert the string version of the number to the integer equivalent, you use the int() function, like so:

```
#convert string to int data type
print(int("7"))

#check the data type with type() method
print(type(int("7")))

#output

#7
#<class 'int'>
```
