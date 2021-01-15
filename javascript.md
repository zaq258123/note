# Javascript

### OOP \(Object-oriented programming\)

物件導向程式設計中包含各種獨立而又互相呼叫的物件，以物件模式描述真實系統，並將「抽象化 \(Abstraction\)」、 「封裝 \(Encapsulation\)」 、 「繼承 \(Inheritance\)」 、 「多型 \(Polymorphism\)」的觀念融入系統開發中。



### ASI \(Automatic Semicolon Insertion\)

return 宣告會受自動插入分號（automatic semicolon insertion，ASI）影響。  
No line terminator is allowed between the return keyword and the expression.

```javascript
return
a + b;
```

會因為 ASI 而變成：

```javascript
return;
a + b;
```

要避免 ASI 問題，可以添加括號：

```javascript
return (
  a + b
);
```



### IIFEs \(Immediately Invoked Functions Expressions\)

```javascript
// Function Statement
function sayHello(name) {
  console.log('Hello ' + name);
}
sayHello('IIFEs');

// Function Expression;
var sayWelcome = function(name) {
  console.log('Welcome, ' + name);
};
sayWelcome('IIFEs');
console.log(sayWelcome);

// Immediately Invoked Functions Expressions (IIFEs)
var sayWelcomeIIFEs = (function(name) {
  return 'Welcome, ' + name;
})('IIFEs');

// Throw Error HERE!!
console.log(sayWelcomeIIFEs());

//Expression
(function(name) {
  console.log('Welcome, ' + name);
})('IIFEs');
```



### Closure

* [part 1](https://pjchender.blogspot.com/2016/05/javascriptclosures.html)
* [part 2](https://pjchender.blogspot.com/2016/05/javascriptclosures.html)
* [part 3](https://pjchender.blogspot.com/2016/05/javascriptclosures.html)
* [part 4](https://pjchender.blogspot.com/2016/05/javascriptclosures.html)

