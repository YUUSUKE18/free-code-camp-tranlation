# Python Convert String to Int – How to Cast a String in Python

When you're programming, you'll often need to switch between data types.
The ability to convert one data type to another gives you great flexibility when working with information.
There are different built-in ways to convert, or cast, types in the Python programming language.
In this article, you'll learn how to convert a string to an integer.
Let's get started!

プログラミングを行っている時、データの型の変換が必要となることがあるでしょう。
あるデータ型を他のデータ型に変換する知識・経験は、情報を扱うときに、プログラマーにとって、データに対して、柔軟に対応できるようになります。
Python というプログラミング言語において、型を変換、そして、キャストするといった多様な方法が組み込まれています。
この記事では、String 型を Int 型に変換する方法について、学べます。
それでは、詳しく見てきましょう。

## Data types in Python

Python supports a variety of data types.
Data types are used for specifying, representing, and categorizing the different kinds of data that exist and are used in computer programs.
Also, different operations are available with different types of data – one operation available in one data type is often not available in another.

One example of a data type is strings.
Strings are sequences of characters that are used for conveying textual information.
They are enclosed in single or double quotation marks, like so:

Python は、様々なデータの型をサポートしています。
データの型は、コンピュータプログラムで使われている、そして、存在している異なるタイプのデータの型を特定、再表示、区別するのに使われています。
また、あるデータ型で利用できる処理が、別のデータ型では利用できないといったデータ型によって利用できる処理が異なります。

データの型の一例として、String 型があります。
String 型は、テキストベースの情報を扱うのに使われている文字列となります。
String 型は、以下のコードのように、シングル、あるいは、ダブルクォテーションで囲われます。

Ints, or integers, are whole numbers.
They are used to represent numerical data, and you can do any mathematical operation (such as addition, subtraction, multiplication, and division) when working with integers.
Integers are not enclosed in single or double quotation marks.

Int 型や integers は、整数となります。
整数は、数値データを表すのに使われます。そして、数字を取り扱うときに、＋、ー、✖︎、÷ といった四則演算で使うことができます。
整数は、シングル、あるいはダブルクオテーションで囲われません。

## Data type conversion

Sometimes when you're storing data, or when you receive input from a user in one type, you'll need to manipulate and perform different kinds of operations on that data. Since each data type can be manipulated in different ways, this often means that you'll need to convert it. Converting one data type to another is also called type casting or type conversion. Many languages offer built-in cast operators to do just that – to explicitly convert one type to another.

データを保存するとき、あるいは、入力された型データを受け取るとき、そのデータにさまざまな操作を行う必要もあるでしょう。型データによって、対応できる処理とできない処理がある、データ型を変更する必要があります。あるデータ型から他のデータ型への変換は、型のコンバージョンあるいはキャストとも言われています。多くのプログラミング言語では、ある型から他の型への変換を組み込みの機能として、提供しています。

## How to convert a string to an integer in Python

To convert, or cast, a string to an integer in Python, you use the int() built-in function. The function takes in as a parameter the initial string you want to convert, and returns the integer equivalent of the value you passed. The general syntax looks something like this: int("str"). Let's take the following example, where there is the string version of a number:

Python で文字型を数値型へ変換するためには、組み込み関数である int()を使います。この組み込み関数は、型変換したい文字列を引数として、数値としての値を戻します。一般的な文法は、int("str")となります。それでは、数値が文字列となっている次の例を参考に見ていきましょう。

#string version of the number 7
print("7")

#check the data type with type() method
print(type("7"))

#output

#7
#<class 'str'>

To convert the string version of the number to the integer equivalent, you use the int() function, like so:

文字列の状態の数字を型変換するために、以下のように int()関数を使います。

#convert string to int data type
print(int("7"))

#check the data type with type() method
print(type(int("7")))

#output

#7
#<class 'int'>

# A practical example of converting a string to an int

Say you want to calculate the age of a user. You do this by receiving input from them. That input will always be in string format.

So, even if they type in a number, that number will be of <class 'str'>.

If you want to then perform mathematical operations on that input, such as subtracting that input from another number, you will get an error because you can't carry out mathematical operations on strings.

Check out the example below to see this in action:

The error mentions that subtraction can't be performed between an int and a string.

You can check the data type of the input by using the type() method:

The way around this and to avoid errors is to convert the user input to an integer and store it inside a new variable:

例えば、利用者の年齢を計算したいとしましょう。入力された値を受け取った時に、計算を実行できます。入力される型は、いつも文字型となります。
数字で入力されたとしても、受け取る型は、<class 'str'>となります。
他の入力された数字から引き算するなど、もし、入力時に計算処理を実行したいならば、文字型では、計算処理を行えないので、エラーとなります。
以下のサンプルコードをご覧ください。

Int 型と String 型の引き算は、実行できないエラーとなります。

type()を使うことで、入力されたデータ型を確認できます。

このエラーを避けるためには、利用者の入力を Int 型に変換し、新しい変数内に変換したデータを保存します。

# Conclusion

And there you have it - you now know how to convert strings to integers in Python!

If you want to learn more about the Python programming language, freeCodeCamp has a Python Certification to get you started.

You'll start with the fundamentals and progress to more advance topics like data structures and relational databases. In the end, you'll build five projects to practice what you learned.

Thanks for reading and happy coding!

Python で文字型から数字型へ変換する方法が分かりましたね。
もし、Python をもっと学びたいならば、freeCodeCamp では、Python の認定コースがあります。
Python の基礎から始めて、リレーショナルデータベースやデータ構造といった高度なトピックへと進んでいきます。
最後には、実践へとつなげるために、5 つのプロジェクトを作成します。

ここまで読んでくださってありがとうございます、そして、コーディングを楽しみましょうね！
