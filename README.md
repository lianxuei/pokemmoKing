# xsl-img

#### 介绍
用来保存小森灵图片资源和更新接口文件的仓库

#### 使用说明

##### wrap-version-update插件接口返回说明

```json
请求接口：
https://appsapi.seepine.com/v1/check?id=552311023296581&version=7.8.5
{
  "code": 0,
  "data": {
    "appId": "552311023296581",
    "appName": "天王APP",
    "needUpdate": false,
    "version": "7.8.5",
    "tip": "传入版本号[7.8.5]大于正式版[6.6.6]，认为是测试版本，无需更新",
    "isTest": true
  }
}
https://appsapi.seepine.com/v1/check?id=552311023296581
{
  "code": 0,
  "data": {
    "appId": "552311023296581",
    "appName": "天王APP",
    "needUpdate": true,
    "version": "1.0.3",
    "description": "1.更换热更新组件\n2.xxxxxx\n3.xxxxxx",
    "pkgUrl": "https://zws.im/󠁿󠁡󠁵󠁶󠁱󠁶󠁧",
    "wgtUrl": "https://zws.im/󠁿󠁡󠁵󠁶󠁱󠁶󠁧",
    "isHBuilderUpdate": true,
    "isForceUpdate": true,
    "tip": "未传版本号，直接返回正式版，且强制需要更新"
  }
}
isHBuilderUpdate-->决定是否全局更新
isForceUpdate-->决定是否强制更新
pkgUrl-->全局更新文件，apk
wgtUrl-->热更新文件，wgt
```

```json
{
  "code": 0,
  "data": {
    "appId": "552311023296581",
    "appName": "天王APP",
    "needUpdate": true,
    "version": "1.0.3",
    "description": "1.更换热更新组件\n2.xxxxxx\n3.xxxxxx",
    "pkgUrl": "https://zws.im/󠁿󠁡󠁵󠁶󠁱󠁶󠁧",
    "wgtUrl": "https://zws.im/󠁿󠁡󠁵󠁶󠁱󠁶󠁧",
    "isHBuilderUpdate": true,
    "isForceUpdate": true,
    "tip": "未传版本号，直接返回正式版，且强制需要更新"
  }
}
```

##### 

```json
{
  "code": 0,
  "data": {
    "appId": "552311023296581",
    "appName": "森灵图鉴单机版本",
    "needUpdate": true,
    "version": "1.0.3",
    "description": "1.更换热更新组件",
    "pkgUrl": "https://zws.im/󠁿󠁡󠁵󠁶󠁱󠁶󠁧",
    "wgtUrl": "https://zws.im/󠁿󠁡󠁵󠁶󠁱󠁶󠁧",
    "isHBuilderUpdate": true,
    "isForceUpdate": true,
    "tip": "未传版本号，直接返回正式版，且强制需要更新"
  }
}
```

##### yzhua006-upddate插件接口返回说明

0为false，1为true

```
version: '1.0.2', //线上版本
                        now_url: "https://dldir1.qq.com/weixin/android/weixin802android1860_arm64.apk", //更新链接
                        silent: 0, //是否是静默更新
                        force: 1, //是否是强制更新
                        net_check: 1, //非WIfi是否提示
                        note: "产品汪汪要改这个字的颜色", //更新内容
```



```json
{
	"version": "1.0.7", 
	"now_url": "https://zc-oss2.oss-cn-hongkong.aliyuncs.com/119%E7%89%88%E6%9C%AC.apk", 
	"silent": 0, 
	"force": 0,
	"net_check": 1,
	"note": "更新啦" 
}
```
##### 小森灵事件提醒接口返回说明
code决定提示框的显示次数，deleteCode帮助用户删除上次的缓存，每次更新记得同步增加
needRemind决定是否开启提醒
description为提醒内容
imageUrl为提醒内容图片
```json
{
    "code": "0",
    "date": "2024-06-05",
    "deleteCode": "-1",
    "needRemind": true,
    "data": {
        "name": "小森灵事件提醒",
        "description": "签到活动今日（6.4）结束",
        "imageUrl": "https://pic.imgdb.cn/item/665ed1e95e6d1bfa052ecd4b.jpg",
        "tip": "未传版本号，直接返回正式版，且强制需要更新"
    }
}
```


#### 参与贡献

1.  Fork 本仓库
2.  新建 Feat_xxx 分支
3.  提交代码
4.  新建 Pull Request


#### 特技

1.  使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2.  Gitee 官方博客 [blog.gitee.com](https://blog.gitee.com)
3.  你可以 [https://gitee.com/explore](https://gitee.com/explore) 这个地址来了解 Gitee 上的优秀开源项目
4.  [GVP](https://gitee.com/gvp) 全称是 Gitee 最有价值开源项目，是综合评定出的优秀开源项目
5.  Gitee 官方提供的使用手册 [https://gitee.com/help](https://gitee.com/help)
6.  Gitee 封面人物是一档用来展示 Gitee 会员风采的栏目 [https://gitee.com/gitee-stars/](https://gitee.com/gitee-stars/)
