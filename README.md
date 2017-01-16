# 布局
##计算页面大小，算出font-size
```javascript

! function(n, e) {
    var t = n.documentElement,
        i = "orientationchange" in window ? "orientationchange" : "resize",
        d = function() {
            var n = t.clientWidth;
            if (n) {
                var e = 100 * (n / 320);
                e > 200, t.style.fontSize = e + "px"
            }
        };
    n.addEventListener && (e.addEventListener(i, d, !1), n.addEventListener("DOMContentLoaded", d, !1))
}(document, window); 
```
##根据font-size 转换成 用rem来布局页面

示例/event/faction.htm
