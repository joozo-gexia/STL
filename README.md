## STL with H5Shwo and H5Site
STL(SiteServer Template Language),Here are the main instructions on how to use H5Show STL and H5Site, unlike the CMS STL SiteServer syntax, such as the need to see the STL SiteServer syntax, please log http://stl.siteserver.cn view. Welcome to questions and Bug, thank you

###General code
####How to add template data
We add template data by writing the JSON file, as shown in the code.
The  field ‘categoryName’ is template type, which is generally classified as the style of the template. 
For example "categoryName": "科技";
The field 'categorySN' is template directory, This directory and the categoryName fields above are corresponding.
The 'templates' There is specific templates list. According to the following format, fill in templateName,templateSN,items,thumbUrl... OK.
```json
[
    {
        "categoryName": "科技",
        "categorySN": "technology",
        "templates": [
            {
                "templateName": "gx-exponent",
                "templateSN": "h5siteasdf000001",
                "items": 7,
                "thumbUrl": "template.jpg",
                "templateUrl": "",
                "description": ""
            },
            {
                "templateName": "gx-nike",
                "templateSN": "h5siteasdf000002",
                "items": 9,
                "thumbUrl": "template.jpg",
                "templateUrl": "",
                "description": ""
            }
        ]
    }
]
```
The directory structure
```html
index.json
technology
-H5SITEASDF000001 (templateSN is template folder name)
--1.html
--2.html (items is the total number of HTML files)
--template.jpg (thumbUrl is template thumbnail name)
-H5SITEASDF000002
-...
```

####H5Show use of with STL
##### How to define the code for a different devices by STL 
//the common code
```html
<stl:config>
    <stl:style height="100%" backgroundUrl="{stl.templateUrl}/images/themebicycle1.jpg" backgroundSize="cover" animationName="fadeIn" animationDuration="1s" animationTimingFunction="ease" animationDelay="0" animationIterationCount="2">	
        background-position:0 bottom; 
        background-repeat:no-repeat; 
        box-sizing:border-box;
    </stl:style>
</stl:config>
```
//for phone
```html
<stl:style mediaType="phone"></stl:style>
```
//for pad
```html
<stl:style mediaType="pad"></stl:style>
```
//for pc
```html
<stl:style mediaType="pc"  width="420px" margin="0 auto"></stl:style>
```
```

##### How to obtain the specific content 
###### For example TEXT 
``` html
    <stl:text>
       <stl:style fontFamily="Microsoft Yahei" marginTop="6px" animationName="fadeInRight" animationDuration="1s" animationTimingFunction="linear" animationDelay="1s" animationIterationCount="1"> display: block; </stl:style>
        <stl:style mediaType="phone" fontSize="30px" ></stl:style>
        <stl:style mediaType="pad" fontSize="45px" ></stl:style>
        <stl:style mediaType="pc" fontSize="50px" ></stl:style>
        GRADE  //here is the specific content 
    </stl:text>
```

    As mentioned in the above code, the content area of the plain text we can use the text label to obtain. A text style definitions the following example put it wrote tags. Here we need to use the "Hump" writing, [Hump Code]. that attributes if there are two or more words composition is the "-" to remove, and put the second word in the first letter of the alphabet size. For example: font-family:"Microsoft Yahei"; We need to write：fontFamily="Microsoft Yahei".
    
    STL some tags can be a single label, but some contain other labels must be written into the label. For example:

Yes
```html
1、<stl:style mediaType="phone" fontSize="30px" ></stl:style>
2、<stl:style mediaType="phone" fontSize="30px" />
3、<stl:style mediaType="phone">font-size:30px;</stl:style>

No
1、<stl:style mediaType="phone" fontSize="30px"> // Although there is no containing the content, but the syntax is incorrect, if single label, need to use /> to end tag.
2、<stl:style mediaType="phone">font-size:30px;  //The tag contains the content, and can not be used in a single label
```
Note: We strongly suggest that you use the "Hump the wording" to write the style to the STL grammar, so in the "Gexia platform, modifications, will display default values. It will also be easy to modify. There will not be many useless code in the page. For example:

```html
<stl:style height="100%" backgroundUrl="{stl.templateUrl}/images/themebicycle1.jpg" backgroundSize="100% 100%" paddingTop="40px" lineHeight="1.5" animationName="fadeInUp" animationDuration="1s" animationTimingFunction="ease" animationDelay="0" animationIterationCount="2" />
```

###### <stl:text></stl:text>  | <stl:text />  and <stl:textarea></stl:textarea>
//Writing one <stl:text></stl:text>
```html
    <stl:text>
       <stl:style fontFamily="Microsoft Yahei" animationName="fadeInLeft" animationDuration="1s" animationTimingFunction="linear" animationDelay="1s" animationIterationCount="1"></stl:style>
        <stl:style mediaType="phone" fontWeight="700" fontSize="30px" margin="0 0 0 10%"></stl:style>
        <stl:style mediaType="pad" padding="20px 0 20px 5%" fontSize="45px"  fontWeight="700" margin="0 auto" width="420px" fontSize="60px">
        </stl:style>
        <stl:style mediaType="pc" padding="20px 0 20px 5%" fontSize="45px"  fontWeight="700" margin="0 auto" width="420px" fontSize="60px"></stl:style>
        品位
    </stl:text>
```    
//Writing two <stl:text></stl:text>
```html
<stl:config>
    <stl:style>
        .unmberone {
            color: #626c6e;
        }
    </stl:style>
    <stl:style mediaType="pc">       
        .unmberone{
            line-height: 70px;
        }
    </stl:style>
    <stl:style mediaType="pad">
        .unmberone{
            min-height: 500px;
        }
    </stl:style>
    <stl:style mediaType="phone">
        .unmberone{
            font-size: 16px;
        }
    </stl:style>
</stl:config>
//html code one
<div class="numberone">
    <stl:text>
            成为中国软件行业最具竞争力的企业
    </stl:text>
</div>
```
```html
//html code with other writing
<div class="numberone">
    <stl:text value="成为中国软件行业最具竞争力的企业" />
</div>
```
The <stl:textare /> like the <stl:text>

###### <stl:a></stl:a>
//Writing one
```html
<stl:config>
    <stl:style>
        .unmberone {
            color: #626c6e;
        }
    </stl:style>
    <stl:style mediaType="pc">       
        .unmberone{
            line-height: 70px;
        }
    </stl:style>
    <stl:style mediaType="pad">
        .unmberone{
            min-height: 500px;
        }
    </stl:style>
    <stl:style mediaType="phone">
        .unmberone{
            font-size: 16px;
        }
    </stl:style>
</stl:config>
<stl:a href="http://www.gexia.com" class="unmberone"  style="color:#fff;">
    从这里开始>>
</stl:a>
```
//Writeing two
```html
<stl:a href="http://m.gexia.com" style="color:#fff;">
    <stl:style width="260px" borderRadius="8px" backgroundColor="rgba(255,255,255,0.4)">position: absolute; top: 300px; left: 50%; margin-left: -130px;</stl:style>
    <stl:style mediaType="phone"  height="40px" lineHeight="40px" fontSize="20px"></stl:style>
    <stl:style mediaType="pad"  height="50px" lineHeight="50px" fontSize="30px"></stl:style>
    <stl:style mediaType="pc"  height="50px" lineHeight="50px" fontSize="30px"></stl:style>
    从这里开始>>
</stl:a>
```

###### <stl:image></stl:image>
```html
//Writing one 
<stl:config>
    <stl:style>
        .unmberone {
            color: #626c6e;
        }
    </stl:style>
    <stl:style mediaType="pc">       
        .unmberone{
            line-height: 70px;
        }
    </stl:style>
    <stl:style mediaType="pad">
        .unmberone{
            min-height: 500px;
        }
    </stl:style>
    <stl:style mediaType="phone">
        .unmberone{
            font-size: 16px;
        }
    </stl:style>
</stl:config>

<div class="unmberone">
    <stl:image src="{stl.templateUrl}/images/lijian2_text1.png" />
</div>
```

//Writing two
```html
<stl:image src="{stl.templateUrl}/images/lijian2_text1.png">
    <stl:style />
    <stl:style mediaType="phone" marginTop="10%" />
    <stl:style mediaType="pad" marginTop="10%" width="500px" margin="0 auto" />
    <stl:style mediaType="pc" marginTop="-10%" width="500px" margin="0 auto">z-index: 1;</stl:style>
</stl:image>
```

###### <stl:editor></stl:editor>
//Writing one 
```html
<stl:config>
    <stl:style>
        .unmberone {
            color: #626c6e;
        }
    </stl:style>
    <stl:style mediaType="pc">       
        .unmberone{
            line-height: 70px;
        }
    </stl:style>
    <stl:style mediaType="pad">
        .unmberone{
            min-height: 500px;
        }
    </stl:style>
    <stl:style mediaType="phone">
        .unmberone{
            font-size: 16px;
        }
    </stl:style>
</stl:config>

<div class="unmberone">
    <stl:editor>
        阁下互动产品
    </stl:editor>
</div>
```
//Writing two
```html
    <stl:editor>
        <stl:style  animationName="flip" animationDelay="1s" animationDuration=".5s" margin="0 10%">text-shadow: 9px 9px 2px #dedede, 12px 12px 5px #ccc;</stl:style>
        <stl:style mediaType="phone" fontSize="45px"  />
        <stl:style mediaType="pad"  fontSize="65px"  />
        <stl:style mediaType="pc"  fontSize="65px"  />
        阁下互动产品
    </stl:editor>
```

###### <stl:box></stl:box>
//Writing one 
```html
   <stl:box>
        <stl:data name="title" datatype="text" displayname="标题" value="NIKE FREE iD专属定制" />
        <stl:data name="subtitle" datatype="text" displayname="副标题" value="觉醒天生动力，演绎专属魅力" />
        <stl:data name="url" datatype="text" displayname="链接" value="http://www.gexia.com" />
        <stl:data name="pic" datatype="image" displayname="图片" value="{stl.templateUrl}/images/threeofthreepic.png" />
        <img src="{stl.data.pic}" alt="{stl.data.title}">
            <div class="jo-imgtitle jo-grey">
                <div class="title"><a href="{stl.data.url}">{stl.data.title}</a>
                </div>
                <div class="subtitle"><a href="{stl.data.url}">{stl.data.subtitle}</a>
                </div>
                <a href="{stl.data.url}" class="fa fa-chevron-circle-right"></a>
            </div>
    </stl:box>
```    
Note: About <stl:data> some attribute description
    name: Be arbitrary
    datatype: text | textarea | editor | image
    displayname: Be arbitrary
    value： That is the content of the display
    {stl.data.name}  the name is "name" attribute


###### <stl:editor></stl:editor>
```html
//Writing one 


//Writing two

```

