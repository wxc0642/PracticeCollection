## 转筒案例
1. 根据一定规则，给选定元素下的子元素添加样式，用setAttribute("class","className");
2. 使用for(i in arr)时，使用数组下标会出错
3. 对于要产生3d旋转效果的元素组都要加上`transform-style: preserve-3d;`，否则元素组会堆叠到一起，出现平面旋转效果。


## 相册albem案例
1. 主要是利用js改变选定元素的`left`属性，使元素位置变化
   1.1 必须给元素添加索引，循环，`album[j].index=j;`，赋予元素index属性。
   1.2 根据前一次选择展示内容的index与此次click选中的内容的index进行比较。
        
        若是此次选择的(j)比之前的(i)小:将[j+1,i]向右移动
        若是此次选择的(j)比之前的(i)大:将[i+1,j]向左移动
   
   1.3 js设置、修改、获取元素的style定义的属性
       
       设置、修改：`chosenAfter.style.left=left;`，用`元素.style.属性名=value;`
                `setAttribute()对这种属性不起作用`
       获取:`getComputedStyle(chosenAfter).left`，用`getComputedStyle(元素).属性名`,获取到的是字符串
       对字符串的处理：
       replace\split（去除特定内容，去除分割符）     slice\substr\substring(return 选择截取内容)

2. css选择器  兄弟选择器
   
   `#chosen~div`可以选择到与`id="chosen"`同级的、排序在其后的全部兄弟组件。

3. 使用了`::after`伪元素定义textBox在渲染时的内容

4. 在for循环（索引为i）内，对数组内每一个Node添加onclick回调，在回调函数里面，输出的索引i是(最大索引+1)。

5. 对本例未能用css3实现，借助了js，致使切换展示内容时动作生硬、过渡不自然，以后再尝试只用html+css实现。


## 导航动画 guideAnimation
1. 
