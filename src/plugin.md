<center>插件</center>
==
---

## book.json 插件配置示例
[插件地址](https://plugins.gitbook.com/)
```json
{
  "title": "Markdown分享",
  "description": "Markdown、程序员利器!",
  "language": "zh-hans",
  "plugins": [
    "github"
  ],
  "pluginsConfig": {
    "github": {
      "url": "https://github.com/iyw/markdown.git"
    }
  }
}

```

gitbook默认带以下5个插件
```
highlight
search
sharing
fontsettings
livereload
```
温馨提示:如果需要去掉默认的插件、只需要在配置中加上如下代码
```
"plugins": [
  "-search"
]
```

## 介绍几款插件
##### 1. [github](https://plugins.gitbook.com/plugin/github)
在右上角显示 github 仓库的图标链接
```json
{
    "plugins": [ "github" ],
    "pluginsConfig": {
        "github": {
            "url": "https://github.com/your/repo"
        }
    }
}
```

#### 2. [github-buttons](https://plugins.gitbook.com/plugin/github-buttons)
显示 github 仓库的 star 和 fork 按钮。
```json
{
  "plugins": [
    "github-buttons"
  ],
  "pluginsConfig": {
    "github-buttons": {
      "buttons": [
        {
          "user": "iyd",
          "repo": "markdown",
          "type": "star",
          "size": "large"
        }, 
        {
          "user": "iyd",
          "type": "follow",
          "width": "230",
          "count": false
        }
      ]
    }
  }
}
```
#### 3. [local-video](https://plugins.gitbook.com/plugin/local-video)
使用Video.js 播放本地视频
```
{
    "plugins": [ "local-video" ]
}
```
示例

```
{% raw %}
  <video id="my-video" class="video-js" controls preload="auto" width="800" height="400"
  poster="MY_VIDEO_POSTER.jpg" data-setup="{}">
  <source src="http://yundong.httpds.com/70effb23721b485bbfdcd93e3aa6ed2e/410d466451fa488c8e3f49fe75fb13be-9e9cfd5dc5fd3a12971177a55c4d5916-ld.mp4" type='video/mp4'>
  <p class="vjs-no-js">
    To view this video please enable JavaScript, and consider upgrading to a web browser that
    <a href="http://videojs.com/html5-video-support/" target="_blank">supports HTML5 video</a>
  </p>
  </video>
{% endraw %}
```
{% raw %}
  <video id="my-video" class="video-js" controls preload="auto" width="800" height="400"
  poster="MY_VIDEO_POSTER.jpg" data-setup="{}">
  <source src="http://yundong.httpds.com/70effb23721b485bbfdcd93e3aa6ed2e/410d466451fa488c8e3f49fe75fb13be-9e9cfd5dc5fd3a12971177a55c4d5916-ld.mp4" type='video/mp4'>
  <p class="vjs-no-js">
    To view this video please enable JavaScript, and consider upgrading to a web browser that
    <a href="http://videojs.com/html5-video-support/" target="_blank">supports HTML5 video</a>
  </p>
  </video>
{% endraw %}

#### 4. [Donate](https://plugins.gitbook.com/plugin/donate)
打赏插件
```json
"plugins": [
    "donate"
],
"pluginsConfig": {
    "donate": {
        "wechat": "./wechat.jpeg",
        "alipay": "./alipay.jpeg",
        "title": "",
        "button": "赏",
        "alipayText": "支付宝打赏",
        "wechatText": "微信打赏"
    }
}
```

#### 5. [sharing-plus](https://plugins.gitbook.com/plugin/sharing-plus)
分享当前页面，比默认的 sharing 插件多了一些分享方式
```json
 plugins: ["-sharing", "sharing-plus"]
```

```json
"pluginsConfig": {
    "sharing": {
       "douban": false,
       "facebook": false,
       "google": true,
       "hatenaBookmark": false,
       "instapaper": false,
       "line": true,
       "linkedin": true,
       "messenger": false,
       "pocket": false,
       "qq": false,
       "qzone": true,
       "stumbleupon": false,
       "twitter": false,
       "viber": false,
       "vk": false,
       "weibo": true,
       "whatsapp": false,
       "all": [
           "facebook", "google", "twitter",
           "weibo", "instapaper", "linkedin",
           "pocket", "stumbleupon"
       ]
   }
}
```

#### 6 [chart](https://plugins.gitbook.com/plugin/chart)
使用 C3.js 或者 Highcharts 绘制图形。
```json
{
    "plugins": [ "chart" ],
    "pluginsConfig": {
        "chart": {
            "type": "c3"
        }
    }
}
```
type 可以是 c3 或者 highcharts, 默认是 c3.
示例:
```
{% chart %}
{
    "data": {
        "type": "bar",
        "columns": [
            ["data1", 30, 200, 100, 400, 150, 250],
            ["data2", 50, 20, 10, 40, 15, 25]
        ],
        "axes": {
            "data2": "y2"
        }
    },
    "axis": {
        "y2": {
            "show": true
        }
    }
}
{% endchart %}
```
{% chart %}
{
    "data": {
        "type": "bar",
        "columns": [
            ["data1", 30, 200, 100, 400, 150, 250],
            ["data2", 50, 20, 10, 40, 15, 25]
        ],
        "axes": {
            "data2": "y2"
        }
    },
    "axis": {
        "y2": {
            "show": true
        }
    }
}
{% endchart %}