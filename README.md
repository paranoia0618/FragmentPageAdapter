# FragmentPageAdapter
##底部导航栏+ViewPager滑动切换页面  
###1.*ViewPager的缓存机制*：   
>>ViewPager会缓存当前页，前一页，以及后一页，比如有1，2，3，4这四个页面：  
>>当我们处于第一页：缓存1，2——> 处于第二页：缓存 1，2，3——> 处于第三页：缓存2，3，4 ——> 处于第四页缓存3，4这样！  
  
    
###2.*使用PagerAdapter要重写相关方法*：  
>>getCount( ):获得viewpager中有多少个view  
>>destroyItem( ):移除一个给定位置的页面.  
>>instantiateItem( ):①将给定位置的view添加到ViewGroup(容器)中,创建并显示出来 
>>>>>>>>②返回一个代表新增页面的Object(key),通常都是直接返回view本身就可以了, 也可以自定义自己的key,但是key和每个view要一一对应的关系  
  
  >>isViewFromObject( ):判断instantiateItem(ViewGroup, int)函数所返回来的Key与一个页面视图是否是代表的同一个视图(即它俩是否是对应的，对应的表示同一个View),通常我们直接写 return view == object；就可以了  
  
  ###3.效果  
  实现效果图：  
  ![实现效果图](https://raw.githubusercontent.com/paranoia0618/image/master/85621650.gif)  
  项目结构图：  
  ![项目结构图](http://www.runoob.com/wp-content/uploads/2015/08/383165.jpg)
  
  
