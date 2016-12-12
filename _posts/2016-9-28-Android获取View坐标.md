---
layout: post
title: Android获取View坐标
---

在开发过程中我们会存在获取View的坐标位置的需求。通过查找资料发现View具有getLeft()、getTop()等一系列的方法来获取到View的坐标。但是，在代码中使用时。发现上面方法获取到的值都是0。  

在[StackOverFlow](http://stackoverflow.com/questions/12052570/getright-getleft-gettop-returning-zero)中找到了答案。获取View的坐标需要在`Measure`与`Layout`完成之后。  
而它们的执行都晚于`onCreate`(在`onResume`中也是不能获取到View坐标的）。Activity中有一个方法`onWindowFocusChanged()`是在View绘制完成后执行的，可以在该方法中获取View的坐标。  
```
    @Override
    publicvoid onWindowFocusChanged (boolean hasFocus){
      super.onWindowFocusChanged(hasFocus);
      if(hasFocus){
    	......
      }
    }
```
可以通过`LayoutParams`的`setMargins(left,top,right,bottom)`来设置View的显示位置。


**参考**：    
[Mr_immortalZ](http://blog.csdn.net/mr_immortalz/article/details/51168278)    
[cookiesp](http://cookiesp.pixnet.net/blog/post/96269514)    
[StackOverFlow](http://stackoverflow.com/questions/12052570/getright-getleft-gettop-returning-zero)


