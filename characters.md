#Java Character类
一般情况下，当我们与字符打交道时，我们用原始数据类型char。 

##示例：
```
char ch = 'a';

// Unicode for uppercase Greek omega character
char uniChar = '\u039A'; 

// an array of chars
char[] charArray ={ 'a', 'b', 'c', 'd', 'e' };
```
然而在开发中，我们会遇到我们需要使用对象而不是原始数据类型的情况。为了达到这个需求。Java为原始数据类型char提供了包装类Character。
Character类为操控字符提供了一系列有用处的类（例如：静态类）。你可以借助Character构造函数创造一个Character对象。  
```
Character ch = new Character('a');
```
Java编译器也将能在某些情况下为你创造一个Character对象。例如：如果你将一个原始char传输到一个可预期对象的方法，编译器就会为你自动将char转化成Character. 如果转换从反方向进行，这个特点被称之为自动装箱或拆箱。

## 示例：
```
// Here following primitive char 'a'
// is boxed into the Character object ch
Character ch = 'a';

// Here primitive 'x' is boxed for method test,
// return is unboxed to char 'c'

char c = test('x');
```
## 转义序列：

有反斜杠（\）在前的字符是一个转义序列并且对于编译器有特殊的意义。
换行符(\ n)一直在System.out.println()语句的本教程中经常使用，在字符串打印出来后提前下一行。
以下的表格展示了Java转义序列：  

|转义序列|	描述|
|-------:|------:|
|\t	|在文本中插入一个标签。|
|\b	|在文本中插入一个退格。|
|\n	|在文本中插入一个换行符。|
|\r	|在文本中插入一个回车。|
|\f	|在文本中插入一个换页。|
|\'	|在文本中插入一个单引号字符。|
|\\|	在文本中插入一个反斜杠字符。|

当一个转义序列遇到一个打印语句，编译器就会相应地解译。

##示例：  
如果你想把引号放入引号内，必须使用转义序列,\”,在内部引用:  
```
public class Test {

   public static void main(String args[]) {
      System.out.println("She said \"Hello!\" to me.");
   }
}
```
这将产生以下结果：  
```
She said "Hello!" to me.
```
## Character 方法：  
以下列表是实现Character类所有子类的重要的示例方法： 

|SN   |	方法描述|
|------|------|
|1	|isLetter() <br> 确定具体的char值是一个字母|
|2	|isDigit()  <br> 确定具体的char值是一个数字|
|3	|isWhitespace()<br>确定具体的char值是一个空格|
|4  |isUpperCase()<br>确定具体的char值是一个大写字母|
|5	|isLowerCase()<br>确定具体的char值是一个小写字母|
|6	|toUpperCase()<br>返回指定字符值的大写形式|
|7  |toLowerCase()<br>返回指定字符值的小写写形式|
|8	|toString()<br>返回代表指定的字符值的一个String对象,即一个字符的字符串|

若想查看完整的方法，请参阅java.lang.Character API 规范。  

## 接下来是：  
在一个部分，我们将会浏览Java的String类。你将会学习到如何有效地声明和使用Strings 并且在String类中一些重要的方法。
