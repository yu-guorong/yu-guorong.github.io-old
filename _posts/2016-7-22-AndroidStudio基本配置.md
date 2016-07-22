---
layout: post
title: AndroidStudio基本配置
---
## 配置
**主题**		
`Appearance&Behavior->Appearance`		
![](http://upload-images.jianshu.io/upload_images/1513502-69aff608fa924f18.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**字体**		
Appearance&Behavior->Appearance		
勾选 Override default fonts by (not recommended)		
选择一款支持中文的字体		
![](http://upload-images.jianshu.io/upload_images/1513502-0da36f6b47d5614d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**编辑字体**		
Editor -->Colors & Fonts->Font		
默认是不可更改的，需要选择Save As... 创建一个我们自己的设置	
![](http://upload-images.jianshu.io/upload_images/1513502-135e65cdedb08401.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**显示行号**		
Editor->Appearance，勾选 Show line numbers		

**显示空格**		
Editor->Appearance，勾选 Show white space		

**去除拼写检查**		
Editor->Inspections，取消勾选Spelling		

**自动导包**				
Editor->General->Auto Import，勾选 Add unambiguous improts on the fly

**代码提示**				
Editor->Code Completion  		
Case sensitive completion:		
None为忽略大小写		
All是大小写敏感		
First letter是首字母匹配		

**Logcat显示颜色**		
Editor->Colors&Fonts->Android Logcat		
![](http://upload-images.jianshu.io/upload_images/1513502-7751faa7ca5c95ea.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
不同等级的log设置不同颜色		

**启动不自动打开项目**		
Appearance&Behavior->System Settings		
取消勾选Reopen last project on startup		
![](http://upload-images.jianshu.io/upload_images/1513502-9d23dbfaafcc10b7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## Live Templates		
Editor->Live Templates		
![](http://upload-images.jianshu.io/upload_images/1513502-6c02c5a4906a707b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
新建一个Template Group然后添加Live Template		
![](http://upload-images.jianshu.io/upload_images/1513502-196f74daea5fffa2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


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