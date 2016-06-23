# 图片序列帧特效配置文件


## 参数
### action
#### 详情
|说明|必要|备注|
|---|---|---|
|特效类型|是|--|

#### 取值
|取值|说明|
|---|---|
|imageadmin|图片序列帧|
|playvideo|全屏视频|

### action
#### 详情
|说明|必要|备注|
|---|---|---|
|特效类型|是|--|

#### 取值
|取值|说明|
|---|---|
|imageadmin|图片序列帧|
|playvideo|全屏视频|

### haveoccasion

## JSON Schema
JSON Schema可用于JSON文件的自动化验证。
```
{
   "$schema":"http://json-schema.org/draft-04/schema#",
   "type":"object",
   "properties":{
      "action":{
         "type":"string"
      },
      "haveoccasion":{
         "type":"integer"
      },
      "param":{
         "type":"array",
         "items":{
            "type":"object",
            "properties":{
               "images":{
                  "type":"array",
                  "items":{
                     "type":"string"
                  }
               },
               "event":{
                  "type":"string"
               },
               "eventoccasion":{
                  "type":"integer"
               },
               "fps":{
                  "type":"integer"
               },
               "index":{
                  "type":"integer"
               },
               "r":{
                  "type":"integer"
               },
               "s":{
                  "type":"array",
                  "items":{
                     "type":"number"
                  }
               },
               "h":{
                  "type":"array",
                  "items":{
                     "type":"number"
                  }
               }
            },
            "required":[
               "images",
               "event",
               "eventoccasion",
               "fps",
               "index",
               "r",
               "s",
               "h"
            ]
         }
      }
   },
   "required":[
      "action",
      "haveoccasion",
      "param"
   ]
}
```