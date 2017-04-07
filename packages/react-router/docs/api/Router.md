# &lt;Router>
# &lt;路由>
The common low-level interface for all router components. Typically apps will use one of the high-level routers instead:</br>所有路由组件共同的基础接口。一般app使用高级router中的一个接口
- [`<BrowserRouter>`](../../../react-router-dom/docs/api/BrowserRouter.md)
- [`<HashRouter>`](../../../react-router-dom/docs/api/HashRouter.md)
- [`<MemoryRouter>`](MemoryRouter.md)
- [`<NativeRouter>`](../../../react-router-native/docs/api/NativeRouter.md)
- [`<StaticRouter>`](StaticRouter.md)

The most common use-case for using the low-level `<Router>` is to
synchronize a custom history with a state management lib like Redux or Mobx. Note that this is not required to use state management libs alongside React Router, it's only for deep integration.</br>使用基础`<Router>`最常见的用例是使用类似于Rudex或者Mobx的状态管理库去同步自定义hitory。注意伴随React Router使用状态管理库不是必须的，它只是为了深度集成。
```js
import { Router } from 'react-router'
import createBrowserHistory from 'history/createBrowserHistory'

const history = createBrowserHistory()

<Router history={history}>
  <App/>
</Router>
```

## history: object


A [`history`](https://github.com/ReactTraining/history) object to use for navigation.</br>history对象用在导航
```js
import createBrowserHistory from 'history/createBrowserHistory'

const customHistory = createBrowserHistory()
<Router history={customHistory}/>
```

## children: node

A [single child element](https://facebook.github.io/react/docs/react-api.html#react.children.only) to render.</br>只会渲染唯一一个子元素
```js
<Router>
  <App/>
</Router>
```
