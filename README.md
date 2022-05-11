# dplus
埋点

### 1、浏览器直接引入
```
<script src="./js/dplus.js"></script>
```

## 使用说明

### 1、初始化（用户登录后操作，其余的埋点操作均需保证在此操作之后）
```
dplus.init({
  appkey: "", //申请的appkey
  username: "", //登录的用户名
  area: '330100', //areacode
})
```

### 2、页面埋点
页面进入埋点

```
dplus.beginLogPageView({
  pageName: 'loginview'//自定义的页面的名称
})      
```

页面离开埋点
```
dplus.endLogPageView({
  pageName: 'loginview'//自定义的页面的名称 和页面进入埋点的自定义名称一致
})
```

#### !页面进入和离开埋点需要成对出现才能生效
### 3、事件埋点
```
dplus.eventLog({
  eventName:'',//自定义的埋点事件名称
})
```
### 4、自动上报
系统会自动收集 window.onerror 进行错误上报
系统会自动监听收集window.onunload 进行上报
