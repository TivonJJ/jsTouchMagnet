jsTouchMagnet
=============
仿zaker的 js版磁贴组件。仅仅对移动设备有最好支持

使用方法
```
var t = new TouchMagnet(container,option);
```

container: 磁贴容器，可以填写id或dom对象。 <font color="red">此容器必须是absolute或relative定位的！</font>

option: 选填
 
- numColumns:每一行元素的最大个数，超出就换行。自动排列为"auto";
- columnWidth:列宽，即每一列元素最大的宽度,不包含间距在内。默认320
- verticalSpacing：元素行间距 默认10
- horizontalSpacing：元素列间距 默认10
- xSpacing：容器上下间距 默认8
- ySpacing：容器左右间距 默认8
- draggable：全局拖曳开关 默认true
- bounce: 弹跳效果
- duration：顶部偏移位置 容器距离顶部的位置
- offsetTop：顶部偏移位置 容器距离顶部的位置
- itemHoldTimeout：元素长按事件触发所需时间 默认300ms
- replaceDelay:替换元素时悬停时间,可无或0,如有时间最低为200
- replaceable:元素是否可替换
- wrapperHeight：容器高度，不填将会自动获取
- wrapperWidth：容器宽度，不填将会自动获取


添加一个磁贴
```
t.add(item,option)
```

item:磁贴dom对象，你可以构建任意块来作为磁贴，支持非规则九宫格，可以长方形，正方形混排！

option: 选填

- height:元素高度，不包含间距。
- width:元素宽度，不包含间距。
- x:元素相对于X轴的坐标位置。
- y:元素相对于y轴的坐标位置。
- draggable:是否允许拖曳，如果不允许则不会存入坐标队列中。默认为true
- overflow:overflow属性

方法：

- add(item,option) 添加一个磁贴元素
- remove(item) 移除一个磁贴元素
- removeAll() 移除所有磁贴元素
- pop() 移除最后磁贴元素
- get(index) 根据下标获取对应的磁贴元素
- size() 磁贴总个数
- indexOf(item) 获取磁贴下标位置
- destroy() 销毁磁贴组
- replace(a,b) 替换磁贴元素，位置互换

事件，Eevnts

- addpage： 新增分页
- pagedown：向后翻页
- pageup：向前翻页
- poppage：移除分页
- dragstart：滑页开始
- dragmove：滑页移动
- dragend：滑页结束

- removeitem：移除一个元素
- destory：销毁
- focusitem：元素获得焦点
- dragitem：拖拽元素
- tapitem：点击元素
- holditem：长按元素
- releaseitem：手指在元素上松开

添加事件
`
t.bind(evnt,callback)
`
移除事件
`
t.ubind(event,callback)
`
