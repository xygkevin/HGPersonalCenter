
## 主要实现头部视图的下拉放大以及分页控制，同样的场景也适用于淘宝/天猫店铺界面/简书主页

### 1.适配iphone X，关于头部背景放大，可以设置头部背景上下放大／上下左右放大／不放大(具体放大效果可在主控制器中的处理联动代码处设置，已做注释);

### 2.当然不允许头部背景视图放大可以有两种效果：
#### 主控制器处理联动部分，然后在处理头部背景视图的地方不做放大操作；
#### 1⃣️ 禁止tableView的bances，整个页面可以向上滑动，位于初始位置时不可以向下滑动，本demo采用的是这一种情况；这种情况刷新数据可以在这里添加刷新数据的方法，同时在视图上添加hudView刷新动画，可达到比较好的效果。

#### 2⃣️ 不禁止tableView的bances，这种头部效果类似朋友圈，整个页面可以上下滑动，下拉头部背景视图会离开顶部；这种情况刷新数据可以在这里添加刷新数据的方法，同时在头部添加刷新菊花，或者刷新动画，即可满足你的需求。

#### 对于第二种情况（不禁止tableView的bances头部效果），可去看我的另一个库 [PersonalCenter-Extend](https://github.com/ArchLL/PersonalCenter-Extend), 对解决scrollView嵌套滑动手势冲突做了更多的处理

### 3.关于数据刷新问题，在头部视图不下拉放大的情况下，首次点击菜单item的时候完成一次下拉刷新，以及下拉分页控制器完成下拉刷新，这个相对比较麻烦，近期抽时间完成这个功能;

### 4.最新更新内容：优化代码，并将菜单栏由scrollView更换为CollectionView，体验更佳;

![image](https://github.com/ArchLL/ARPersonalCenter/blob/master/show.gif)
