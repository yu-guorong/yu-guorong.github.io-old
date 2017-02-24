---
layout: post
title: ViewPager使用Fragment时预加载问题
---

使用ViewPager与Fragment时，ViewPager默认会对后面的Fragment进行预加载。ViewPager中有一个方法`setOffscreenPageLimit()`来设置预加载Item的数量，默认值为1，当传入值小于1时，并不会生效。

在ViewPager中使用Fragment时，Fragment的生命周期会一直执行到`onResume()`。在切换Fragment时，如果下一个Fragment已经加载完毕，那么Fragment将不会再执行生命周期中的`onResume()`等方法。

在Fragment中有一个方法`setUserVisibleHint(boolean isVisibleToUser)`来处理Fragment可见状态。需注意的是`setUserVisibleHint()`会在`onCreate()`之前执行。我在项目中需要使不同Fragment的状态栏具有不同的效果。更改状态栏的效果需要在`onCreate()`之后实现，因此加入一个`flag`判断Fragment当前是否已经完成初始化。

```java
	boolean isCreated = false;

	@Override
 	public void setUserVisibleHint(boolean isVisibleToUser) {
      super.setUserVisibleHint(isVisibleToUser);
      if (isVisibleToUser && isCreated) {
        //do something
      }
    }

	@Nullable
	@Override
    public View onCreateView(LayoutInflater inflater, @Nullable ViewGroup container, @Nullable 			Bundle savedInstanceState) {
      isCreated = true;
      return super.onCreateView(inflater, container, savedInstanceState);
    }
   
```



