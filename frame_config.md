# 图片序列帧魔法配置文件
序列帧魔法配置文件包含以下定义
+ 特效类型
+ 触发参数
+ 序列帧文件索引
+ 播放参数



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