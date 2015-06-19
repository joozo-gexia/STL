# 如何制作H5site模版

```html
<stl:config>
    <stl:style>
        .mo-max-width { max-width: 1200px; margin: 0 auto; padding: 0 10px; }
    </stl:style>
    <stl:style mediaType="pad"> 
        .mo-menu .ma { padding: 10px 20px; }
    </stl:style>
    <stl:style mediaType="phone">
        .mo-menu .ma { padding: 10px 5px; }
    </stl:style>
</stl:config>

<div class="mo-menu">
    <div class="mo-max-width jo-menu-list">
        <stl:a href="http://www.xxx.com" class="ma">首页</stl:a>
        <stl:a href="http://www.xxx.com" class="ma">男子</stl:a>
        <stl:a href="http://www.xxx.com" class="ma">女子</stl:a>
        <stl:a href="http://www.xxx.com" class="ma">运动</stl:a>
        <stl:a href="http://www.xxx.com" class="ma">定制</stl:a>
    </div>
</div>
```
