```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>{Channel.Title}-{Stl.SiteName}</title>
<meta content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=0" name="viewport" />
    <meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="keywords" content="{stl:value type="META_KEYWORDS"}" />
    <meta name="description" content="{stl:value type="META_DESCRIPTION"}" />
    <link rel="stylesheet" href="{Stl.SiteUrl}/css/lib/bootstrap.min.css" />
    <link rel="stylesheet" href="{Stl.SiteUrl}/css/lib/fontawesome/css/font-awesome.min.css" />
    <link href="{Stl.SiteUrl}/css/style.css?123" rel="stylesheet" type="text/css" />
    <link href="{Stl.SiteUrl}/css/layer.css" rel="stylesheet" type="text/css" />
<style rel="stylesheet" type="text/css">
@media only screen and (max-width: 768px) {
.cor_nono { display: none;}
}
</style>
    <script src="{Stl.SiteUrl}/js/jquery-1.9.1.min.js" type="text/javascript"></script>
    <script language="javascript" type="text/javascript" src="{Stl.SiteUrl}/js/jquery.SuperSlide.2.1.1.js"></script>
    <script language="javascript" type="text/javascript" src="{Stl.SiteUrl}/js/public.js"></script>
    <script language="javascript" type="text/javascript" src="{Stl.SiteUrl}/js/slide.js"></script>
</head>
<body>
<stl:include file="@/include/header.html"></stl:include>
<div class="main">
<div class="mL">
<stl:dynamic>
  <div class="ml_u1 ml_u1v1">
  <ul>
 <stl:pageContents pageNum="11" scope="All" tags="{Request.tagname}" order="AddDate" groupChannelNot="辅助栏目">
 <stl:if testType="ImageUrl" testOperate="Empty">
 <stl:failureTemplate>
 
 <stl:if testType="IsHot" testOperate="Equals" testValue="true">
 <stl:successTemplate>
 <li class="ml_li2">
 <div class="ml_imgTxt clearfix">
 <stl:a class="fl"><stl:content type="ImageUrl" width="170" height="138"></stl:content></stl:a>
 <div class="ml_p1">
 <div class="ml_t2"><stl:a><stl:content type="Title" wordNum="20"></stl:content></stl:a></div>
 <p><stl:if testType="Summary" testOperate="Empty">
<stl:successTemplate><stl:content type="Content" wordNum="70" isClearTags="true"></stl:content></stl:successTemplate>
<stl:failureTemplate><stl:content type="Summary" wordNum="70"></stl:content></stl:failureTemplate>
</stl:if><stl:a>[详细]</stl:a></p>
 <div class="ml_nn1"><table><tr><td class="mau"><a href="{Stl.SiteUrl}/utils/list.html?Author={Content.Author}" class="cor_blue"><stl:content type="Author"></stl:content></a></td><td> <span class="cor_hs"><stl:content type="AddDate" formatString="yyyy-MM-dd hh:mm"></stl:content></span><span class="cor_hsm"><stl:content type="AddDate" formatString="MM-dd HH:MM"></stl:content></span> &nbsp;</td><td> <a href="#" class="ml_a1 cor_999"><stl:count type="Comments" isDynamic="true"></stl:count></a></td><td><div class="cor_nono"><stl:tags totalNum="4"><stl:a href="{Stl.SiteUrl}/utils/tags.html?tagName={Tag.Name}">{Tag.Name}</stl:a></stl:tags></div></td></tr></table></div>
 </div>
 </div>
 </li>
 </stl:successTemplate>
 <stl:failureTemplate>
     <li>
     <div class="ml_t2"><stl:a><stl:content type="Title" wordNum="28"></stl:content></stl:a></div>
     <div class="ml_imgTxt clearfix">
     <stl:a class="fl"><stl:content type="ImageUrl" width="130" height="86"></stl:content></stl:a>
     <div class="ml_p1">
     <p><stl:if testType="Summary" testOperate="Empty">
<stl:successTemplate><stl:content type="Content" wordNum="50" isClearTags="true"></stl:content></stl:successTemplate>
<stl:failureTemplate><stl:content type="Summary" wordNum="50"></stl:content></stl:failureTemplate>
</stl:if><stl:a>[详细]</stl:a></p>
<div class="ml_nn1"><table><tr><td class="mau"><a href="{Stl.SiteUrl}/utils/list.html?Author={Content.Author}" class="cor_blue"><stl:content type="Author"></stl:content></a></td><td> <span class="cor_hs"><stl:content type="AddDate" formatString="yyyy-MM-dd hh:mm"></stl:content></span><span class="cor_hsm"><stl:content type="AddDate" formatString="MM-dd HH:MM"></stl:content></span> &nbsp;</td><td> <a href="#" class="ml_a1 cor_999"><stl:count type="Comments" isDynamic="true"></stl:count></a></td><td> <div class="cor_nono"><stl:tags totalNum="4"><stl:a href="{Stl.SiteUrl}/utils/tags.html?tagName={Tag.Name}">{Tag.Name}</stl:a></stl:tags></div></td></tr></table></div>
     </div>
     </div>
     </li>
 </stl:failureTemplate>
 </stl:if>
 
 </stl:failureTemplate>
 <stl:successTemplate>
     <li class="ml_li1">
     <div class="ml_t2"><stl:a><stl:content type="Title" wordNum="28"></stl:content></stl:a></div>
     <div class="ml_imgTxt clearfix">
     <div class="ml_p1 add addyan">
     <p><stl:if testType="Summary" testOperate="Empty">
<stl:successTemplate><stl:content type="Content" wordNum="70" isClearTags="true"></stl:content></stl:successTemplate>
<stl:failureTemplate><stl:content type="Summary" wordNum="70"></stl:content></stl:failureTemplate>
</stl:if><br />
       <stl:a>[详细]</stl:a></p>
     <div class="ml_nn1"><table><tr><td class="mau"><a href="{Stl.SiteUrl}/utils/list.html?Author={Content.Author}" class="cor_blue"><stl:content type="Author"></stl:content></a></td><td> <span class="cor_hs"><stl:content type="AddDate" formatString="yyyy-MM-dd hh:mm"></stl:content></span><span class="cor_hsm"><stl:content type="AddDate" formatString="MM-dd HH:MM"></stl:content></span> &nbsp;</td><td> <a href="#" class="ml_a1 cor_999"><stl:count type="Comments" isDynamic="true"></stl:count></a></td><td> <div class="cor_nono"><stl:tags totalNum="4"><stl:a href="{Stl.SiteUrl}/utils/tags.html?tagName={Tag.Name}">{Tag.Name}</stl:a></stl:tags></div></td></tr></table></div>
     </div>
     </div>
     </li>
 </stl:successTemplate>
 </stl:if>
 </stl:pageContents>
 </ul>
<div class="clear"></div>
</div>
<div class="mpage clearfix">
        <stl:pageItems>
            <stl:pageItem type="PreviousPage">
            <stl:successTemplate>
            <a class="fl mpage_prev" href="{Current.Url}">上一页</a>
            </stl:successTemplate>
            <stl:failureTemplate>
            <a class="fl mpage_prev disabled" href="javascript:;">上一页</a>
            </stl:failureTemplate>
            </stl:pageItem>
            <stl:pageItem type="NextPage">
            <stl:successTemplate>
            <a class="fr mpage_next" href="{Current.Url}">下一页</a>
            </stl:successTemplate>
            <stl:failureTemplate>
            <a class="fr mpage_next disabled" href="javascript:;">下一页</a>
            </stl:failureTemplate>
            </stl:pageItem>
        </stl:pageItems>
        </div>
</stl:dynamic>

</div>
<stl:include file="@/include/right_list.html"></stl:include>
<div class="clear"></div>
</div>
<stl:include file="@/include/footer.html"></stl:include>
<!--弹出层 开始-->
<stl:include file="@/include/lay.html"></stl:include>
<!--弹出层 结束-->
</body>
</html>
​<stl:include file="@/include/js.html"></stl:include>

```
