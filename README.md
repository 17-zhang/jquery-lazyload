# jquery-lazyload
jquery图片懒加载插件

###插件描述：
jQuery图片延迟加载插件jQuery.lazyload,使用延迟加载在可提高网页下载速度。在某些情况下，它也能帮助减轻服务器负载。

###使用方法

引用jquery和jquery.lazyload.js到你的页面

1 <script src="jquery-1.11.0.min.js"></script>
2 <script src="jquery.lazyload.js?v=1.9.1"></script>

###html图片调用方法

为图片加入样式lazy  图片路径引用方法用data-original

<img class="lazy" data-original="img/bmw_m1_hood.jpg">
<img class="lazy" data-original="img/bmw_m1_side.jpg">
<img class="lazy" data-original="img/viper_1.jpg">
<img class="lazy" data-original="img/viper_corner.jpg">
<img class="lazy" data-original="img/bmw_m3_gt.jpg">
<img class="lazy" data-original="img/corvette_pitstop.jpg">

###js出始化lazyload并设置图片显示方式


<script type="text/javascript" charset="utf-8">
  $(function() {
      $("img.lazy").lazyload({effect: "fadeIn"});
  });
</script>

###在图片中也可以不使用 class="lazy"，初始化时使用：


$("img").lazyload({effect: "fadeIn"});


###引入

<script src="jquery-1.11.0.min.js"></script>
<script src="jquery.lazyload.js?v=1.9.1"></script>

###路径依据实际目录来确定。

<script type="text/javascript" charset="utf-8">
  $(function() {
      $("img.lazy").lazyload({effect: "fadeIn"});
  });
</script>

###图片引用lazyload 方式

<img class="lazy" data-original="img/bmw_m1_hood.jpg"  />

###参数设置

$("img.lazy").lazyload({
  placeholder : "img/grey.gif", //用图片提前占位
    // placeholder,值为某一图片路径.此图片用来占据将要加载的图片的位置,待图片加载时,占位图则会隐藏
  effect: "fadeIn", // 载入使用何种效果
    // effect(特效),值有show(直接显示),fadeIn(淡入),slideDown(下拉)等,常用fadeIn
  threshold: 200, // 提前开始加载
    // threshold,值为数字,代表页面高度.如设置为200,表示滚动条在离目标位置还有200的高度时就开始加载图片,可以做到不让用户察觉
  event: 'click',  // 事件触发时才加载
    // event,值有click(点击),mouseover(鼠标划过),sporty(运动的),foobar(…).可以实现鼠标莫过或点击图片才开始加载,后两个值未测试…
  container: $("#container"),  // 对某容器中的图片实现效果
    // container,值为某容器.lazyload默认在拉动浏览器滚动条时生效,这个参数可以让你在拉动某DIV的滚动条时依次加载其中的图片
  failurelimit : 10 // 图片排序混乱时
     // failurelimit,值为数字.lazyload默认在找到第一张不在可见区域里的图片时则不再继续加载,但当HTML容器混乱的时候可能出现可见区域内图片并没加载出来的情况,failurelimit意在加载N张可见区域外的图片,以避免出现这个问题.
});


