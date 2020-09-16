# 代码整洁之道 Clean Code

[TOC]

## Chapter1 整洁代码

### 1.什么是整洁代码

*Bjarne Stroustrup:*

**整洁的代码只做一件好事**

1. 减少依赖关系，使之便于维护
2. 依据某种分层战略完善错误处理代码
3. 性能调整至最优，省的引诱别人做没规矩的优化

*Ron Jeddries:*

1. 能够通过所有测试
2. 没有重复代码
3. 体现系统中的全部设计理念
4. 包括尽量少的实体，比如类、方法、函数等



## Chapter2 有意义的命名

1. **名副其实**

   变量、函数、类的名称都应该已经答复了所有的大问题：`why exist; do what; how to use`

   让变量名为自己解释，最好不要让注释解释 

2. **避免误导**

   - 避免使用一些专属名词

     e.g.hp、aix等unix平台的特有词汇

     或使用`accountList`指代账号，除非这真的是个List（会引起错误判断）

   - 提防使用外形相似程度较高的名称

     e.g. `XYZControlForEffiency和XYZControlForEfficiency`

   - 别用小写字母`i`和大写字母`O`作为变量名

3. **做有意义的区分**

   名称相异，那么其代表的意义也应该不同

   反例1：以数字命名，例如`a1`,`a2`等，将其替换为有实际意义的名称会更好，例如`source` `destination`

   反例2：废话`Product` `ProductInfo` `ProductData`这三者明明是一样的意思。同样`getActiveAccount()` `getActiveAccounts()` `getActiveAccountInfo()`也是一样的道理

4. **使用读的出来的名字**

   方便讨论

5. **使用可搜索的名称**

   便于搜索，`MAX_CLASSES_PER_STUDENT`总比数字`7`更加容易定位。同理单字母变量也是一样。

   **单字母名称仅用于短函数中的本地变量，名称长短应该与其作用域大小相对应。**

6. **避免使用编码**

   - 避免使用匈牙利语标记法$\rightarrow$ 类型+名称：bBusy【bool类型，名称含义为Busy的变量】
   - 避免使用成员前缀$\rightarrow$ 不必使用m_来修饰成员变量
   - 接口和实现$\rightarrow$ 例如我在创建一个创建形状用的抽象工厂，该工厂是一个接口，需要使用具体类来进行实现。一般情况下，工厂可以命名为`IShapeFactory`，具体类可以命名为`ShapeFactory`。这里的前导字母`I`可以说是废话，因为不必要让你的读者发现这是一个接口，因此不妨使用`ShapeFactory`即可。

7. **避免思维映射**

   不要让读者在脑子中将你的名称翻译为他们熟知的名称，这种问题经常出现在选择是使用问题领域术语还是解决方案领域术语的时候。

8. **类名的命名方法**

   类名、对象名应该为名词或者是名词短语，不应该为动词

9. **方法(函数)名的命名方法**

   应该为动词和动词短语

10. **别抖机灵**

    不要使用只有自己才能看懂的名称

11. **每个概念对应一个词**

    例如`fetch` `retrieve` `get`都可以表达获取，那么我们在表达获取类中的变量的时候，应该用一直用同一个单词，比如全部都用`get`

    函数名称应该独一无二且要保持一致，这样才能不借助多余的浏览就能找到正确的方法

12. **别用双关语**

    同一个单词最好对应于同一概念

    例如有函数`add`表示为两元素相加，那么函数`insert/append`应当表示为在`list`之后添加

13. **添加有意义的语境**

    添加语境$\rightarrow$ 提供语境$\rightarrow$ 添加前缀。 例如：

    firstName $\rightarrow$ addrFirstName

    lastName$\rightarrow$ addrLastName

    street$\rightarrow$ addrStreet

    houseNumber$\rightarrow$ addrHouseNumber

    或者直接创建一个`Address`类

14. **不必添加没用的意境**

    只要短名称足够清楚，就比长名称好，别给名称添加一些不必要的语境









































