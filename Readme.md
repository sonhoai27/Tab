# sH_Tab Guide

Insert this html code to your html file

```html
  <ul class="nav-tab normal-tab">
    <li class="active"><p>A</p></li>
    <li><p>B</p></li>
    <li><p>C</p></li>
  </ul>
  
  <div class="content-tab">
    <div class="child-tab active">
      <p>This is AAA Tab</p> 
    </div>
    <div class="child-tab">
      <p>This is BBB Tab</p> 
    </div>
    <div class="child-tab">
      <p>This is CCC Tab</p> 
    </div>
  </div>
```

Then insert this javascript code to your js file.
```javascript
$(".normal-tab li").click(function(){var b=$(this).index()+1;$(".normal-tab").each(function(){$(".normal-tab").find("li.active").removeClass("active")}),$(this).addClass("active"),$(".content-tab").each(function(){$(this).find(".child-tab.active").removeClass("active")});$(".content-tab .child-tab:nth-child("+b+")").addClass("active")});
```

And finally insert this css code to your css file.
```css
.nav-tab,.nav-tab>li>p{background:#fafafa;border-radius:4px}.nav-tab{margin-bottom:25px}.nav-tab>li{display:inline-block}.nav-tab>li>p{padding:8px 15px;font-size:14px;margin-bottom:0!important;font-weight:700;transition:all .3s;border:.5px solid #fff}.nav-tab>li>p:hover{cursor:pointer;background:#eee;transition:all .3s}.nav-tab>li.active p{background:#eee;transition:all .3s;border:.5px solid #999}.content-tab .child-tab.active{display:block}.content-tab .child-tab{display:none}
```
