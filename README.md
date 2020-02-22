# music

> A Vue.js project

#使用技术
vue-router vuex es6 webpack 

#页面
推荐页面（上swiper下列表，点击列表，跳转到详情页）<br>
歌手页面（点击歌手列表跳转到歌手详情页）<br>
排行榜页面（上tab切换下排行列表，点击列表跳详情页）<br>
播放器页面（中播放器下播放设置，暂停、上下曲、喜欢等）<br>

#目录
scr{<br>
    api->axios、jsonp, 放后台请求相关配置<br/>
    assets-><br>
    common->stylus{  //放置静态资源 <br>
      base:基础样式文件<br>
      reset:重置样式<br>
      icon:图标<br>
      mixin:定义函数，供调用<br>
      variable:设计规范、定义变量存放公共样式<br>
      
    }
    components->组件<br>
    router->路由<br>
    store->vuex相关代码<br>
}
