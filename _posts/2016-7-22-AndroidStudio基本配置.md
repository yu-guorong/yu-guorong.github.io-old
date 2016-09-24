---
layout: post
title: AndroidStudio基本配置
---
## 配置
**主题**    
`Appearance&Behavior->Appearance`    
![]({{ site.baseurl }}/images/2016-7-22/as1.png)

**字体**    
Appearance&Behavior->Appearance    
勾选 Override default fonts by (not recommended)    
选择一款支持中文的字体    
![]({{ site.baseurl }}/images/2016-7-22/as2.png)

**编辑字体**    
Editor -->Colors & Fonts->Font    
默认是不可更改的，需要选择Save As... 创建一个我们自己的设置    
![]({{ site.baseurl }}/images/2016-7-22/as3.png)

**显示行号**    
Editor->Appearance，勾选 Show line numbers

**显示空格**    
Editor->Appearance，勾选 Show white space

**去除拼写检查**    
Editor->Inspections，取消勾选Spelling

**自动导包**    		
Editor->General->Auto Import    
勾选 Add unambiguous improts on the fly

**代码提示**    
Editor->Code Completion    
Case sensitive completion:    		
None为忽略大小写    
All是大小写敏感    
First letter是首字母匹配    

**Logcat显示颜色**    
Editor->Colors&Fonts->Android Logcat    
![]({{ site.baseurl }}/images/2016-7-22/as4.png)    
不同等级的log设置不同颜色

**启动不自动打开项目**	    
Appearance&Behavior->System Settings    
取消勾选Reopen last project on startup    
![]({{ site.baseurl }}/images/2016-7-22/as5.png)

## Live Templates    
Editor->Live Templates    
![]({{ site.baseurl }}/images/2016-7-22/as6.png)    
新建一个Template Group然后添加Live Template    
![]({{ site.baseurl }}/images/2016-7-22/as7.png)

idd    
```xml
	android:id="@+id/$id$"
```

swc    
```xml
	switch ($data$){    
	  case $value1$:    
	  	break;    
      case $value2$:    
      	break;    
      case $value3$:    
      	break;                
      default:    
      	break;}
```

view		
```xml
	<$viewname$
        android:id="@+id/$id$"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
```
## 插件
### 可禁用插件
Google系插件    	
CVS Integration    CVS版本控制系统    
hg4idea    Mercurial版本控制系统    

### 常用插件

**.ignore**    
配置.gitignore

**ADB idea**    
快捷ADB操作		

**Android ButterKnife Zelezny**    
注解插入		

**GsonFormat**    
按照Gson要求解析String		

**Genymotion**    
使用时配置Genymotion安装路径		

**Android Postfix Completion**    
根据后缀快速完成代码,如系统自带的sout		

**Lifecycle Sorter**    
根据Activity和Fragment的生命周期排序		
快捷键`Ctrl Alt + K`		

**Markdown support**    
Readme.md预览		

**Android Parcelable code generator**    
实现Parcelable接口		

**IdeaVim**    
支持Vim操作		