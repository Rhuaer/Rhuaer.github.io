---
layout:     post
title:      为啥要用Flex布局
date:       2018-5-31
summary:    什么也不写
categories: jekyll pixyll
---

一句话就是Flex布局足够强大，能够覆盖我们大部分的排版需求。

1. 可以直接让子元素水平垂直居中，并且是不用子元素中添加额外的样式代码；
2. 可以使子元素在一个容器中进行经典的类似Grid布局，只要自己发挥聪明才智，使用他提供的属性进行组合就能排版出来；
3. 能够在经典的规则的布局之中容许特殊元素布局，这个对于日常布局中一些差异化排版很有用，主要是应用align-self属性；
4. 能够宽高根据需要进行自适应。只要设置特定的几个属性，就能实现例如如何使用剩余宽高、如何在宽高不足的情况下调整子元素自身大小；

就凭上面这些优点，我能想到的大部分排版需求应该都是能够满足的了，或许吧，后续会把每一种碰到的好玩的布局写法记一下。这里先记录两个Flex布局的教程，相当于日常查询教程吧。

- [Flex 布局教程：语法篇](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)
- [Flex 布局教程：实例篇](http://www.ruanyifeng.com/blog/2015/07/flex-examples.html)

这么好的东西，也多少会有点瑕疵，例如

- 在IE下的兼容。IE10下要求兼容Flex布局就有点蛋疼，一些已知的bug可以在[CanIUse网站](https://caniuse.com/#search=flex)上查询，例如：
  1. 在chrome中长文本能正常换行，但在IE10中，就必须显示给文本元素声明`flex:0 1 auto`
  2. 在IE中，如果使用Flex布局的元素声明了min-height，会导致无法垂直居中，这个需要trick一下，就是顶一个height值比min-height小的值就可以了，例如`min-height:200px; height:10px`
- 学习成本，毕竟那么多属性，然后组合又能多种多样。

但终究还是瑕不掩瑜，用起来。

待补充的好玩用例：