# 序列帧配置文件示例

<!-- toc -->

## 没有特定触发条件的序列帧特效
详情请参考`FaceMagic SDK`中附带的`Kiss`特效。
```json
{
   "action":"imageAmin",
   "param":[
      {
         "images":[
            "qinwen000.png",
            "qinwen001.png",
            "qinwen002.png",
            "qinwen003.png",
            "qinwen004.png",
            ...
            "qinwen148.png",
            "qinwen149.png",
            "qinwen150.png"
         ],
         "fps":25,
         "h":[
            1.03,
            -0.1
         ],
         "s":[
            5.0,
            5.0
         ],
         "r":1,
         "index":270
      }
   ]
}
```
## 指定触发条件的特效动画
详情请参考`FaceMagic SDK`中附带的`大力水手`特效。
```json
{
   "action":"imageamin",
   "haveoccasion":1,
   "param":[
      {
         "images":[
            "dalishuishoumaozi0001.png",
            "dalishuishoumaozi0002.png",
            "dalishuishoumaozi0003.png",
            "dalishuishoumaozi0004.png",
            "dalishuishoumaozi0005.png",
            "dalishuishoumaozi0006.png",
            "dalishuishoumaozi0007.png",
            "dalishuishoumaozi0008.png",
            "dalishuishoumaozi0009.png",
            "dalishuishoumaozi0010.png",
            "dalishuishoumaozi0011.png",
            "dalishuishoumaozi0012.png",
            "dalishuishoumaozi0013.png",
            "dalishuishoumaozi0014.png",
            "dalishuishoumaozi0015.png",
            "dalishuishoumaozi0016.png"
         ],
         "event":"mouthclose",
         "eventoccasion":2,
         "fps":25,
         "s":[
            3.0,
            3.0
         ],
         "h":[
            0.0,
            1.6
         ],
         "r":1,
         "index":290
      },
      {
         "images":[
            "dalishuishouyandou0001.png",
            "dalishuishouyandou0002.png",
            "dalishuishouyandou0003.png",
            "dalishuishouyandou0004.png",
            "dalishuishouyandou0005.png",
            "dalishuishouyandou0006.png",
            "dalishuishouyandou0007.png",
            "dalishuishouyandou0008.png",
            "dalishuishouyandou0009.png",
            "dalishuishouyandou0010.png",
            "dalishuishouyandou0011.png",
            "dalishuishouyandou0012.png",
            "dalishuishouyandou0013.png",
            "dalishuishouyandou0014.png",
            "dalishuishouyandou0015.png",
            "dalishuishouyandou0016.png"
         ],
         "event":"mouthclose",
         "eventoccasion":1,
         "fps":25,
         "index":220,
         "r":1,
         "s":[
            1.7,
            1.7
         ],
         "h":[
            -1,
            0.1
         ]
      }
   ]
}
```
## 序列帧配置文件 JSON Schema
JSON Schema可用于JSON文件的自动化验证。
```json
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