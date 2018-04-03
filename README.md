# 微信小程序 wepyjs 第三方 动态匹配输入框插件

### 效果：
![mark](http://oyz3pjs26.bkt.clouddn.com/blog/180403/3h49h28LjA.gif)






## 使用

### 安装组件
```
npm install wepy-match-input --save
```

### 引入组件
```javascript
<template>
    <wepyMatchInput :params.sync="inputPrams"></wepyMatchInput>
</template>
<script>
    import wepy from 'wepy';
    import wepyMatchInput from 'wepy-match-input';

    export default class Index extends wepy.page {
        data={
            inputPrams:{
                    matchList:[],
                    keyWord:'',
                    keyName:'bookName',
                    placeholder:"请填写书名"
            },
        }
        components = {
            nices
        };
        
        onLoad(){
            
        }
        
        events={
            wepyMatchInputTapCallBack(data,index){
                
            },
            wepyMatchInputFocusCallBack(value){
                
            },
            wepyMatchInputChangeCallBack(value){
                
            },
            wepyMatchInputBlurCallBack(value){
                
            },
            wepyMatchInputConfirmCallBack(value){
                
            }
        }
        
       
    }
    
</script>
```


---------------------------------------

# 字段/Attr


|                  字段                  |           描述           | 必填 | 类型   |             默认              |
| :------------------------------------: | :----------------------: | :--: | ------ | :---------------------------: |
|             params.keyWord             |       当前输入框值       |  是  | string |              ''               |
|             params.keyName             |    匹配列表输出的字段    |  否  | string |             name              |
|            params.matchList            |         匹配列表         |  是  | array  |              []               |
|           params.placeholder           |   input框的placeholder   |  否  | string |              ''               |
| params.tapMatchListItemCallBackFunName | 点击匹配列表项回调方法名 |  否  | string |   wepyMatchInputTapCallBack   |
|  params.tapInputFocusCallBackFunName   |  input focus方法回调名   |  否  | string |  wepyMatchInputFocusCallBack  |
|  params.tapInputChangeCallBackFunName  |  input change方法回调名  |  否  | string | tapInputChangeCallBackFunName |
|   params.tapInputBlurCallBackFunName   |  input blur 方法回调名   |  否  | string |  wepyMatchInputBlurCallBack   |
| params.tapInputConfirmCallBackFunName  | input confirm方法回调名  |  否  | string | wepyMatchInputConfirmCallBack |



# 方法/methods

- 一下方法请放在父级events对象调用。

- 有传方法名的对应方法名，没有传使用的默认方法名。（主要考虑到一个页面有多个时需要自定义以免冲突）

- 以下以默认方法名为例

- |            方法名             |         描述          |            参数             |
  | :---------------------------: | :-------------------: | :-------------------------: |
  |   wepyMatchInputTapCallBack   |  点击匹配列表项回调   | （当前项对象，当前项index） |
  |  wepyMatchInputFocusCallBack  |  input focus方法回调  |      （当前输入框值）       |
  | tapInputChangeCallBackFunName | input change方法回调  |      （当前输入框值）       |
  |  wepyMatchInputBlurCallBack   |  input blur 方法回调  |      （当前输入框值）       |
  | wepyMatchInputConfirmCallBack | input confirm方法回调 |      （当前输入框值）       |

  ​

  ​


[本人博客：callmesoul.cn](http://callmesoul.cn)

![toast](http://nowechat.oss-cn-shenzhen.aliyuncs.com/qrcode_for_gh_b4c00b84720c_258.jpg)

