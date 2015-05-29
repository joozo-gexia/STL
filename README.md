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
