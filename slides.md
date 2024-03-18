---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides, markdown enabled
title: 前端开发技术简介
info: 前端开发技术简介
# apply any unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
---

# 前端开发技术简介

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    立刻开始 <carbon:arrow-right class="inline"/>
  </span>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# 前端 VS 后端

现在的前端其实是个很大的范畴，包括 Web、移动端（Hybrid App）、游戏，桌面端(Electron)、小程序等。

- Web前端开发是针对浏览器的开发，代码在浏览器运行，主要实现用户界面，展示信息，响应用户操作。
- 后端开发是针对服务器的开发，代码在服务器运行，主要实现业务逻辑，对数据进行增删改查，存取读写。

<img src="/WX20240318-012440@2x.png" class="w-600px m-auto mt-20px">

---

# 前端的发展

## Web 1.0 前端工程师 = 网页设计师

早期受制于浏览器以及技术、兼容性等问题，导致网页的显示效果非常的单一，几乎都是静态页面，前端的工作也是非常简单，说是前端，其实只是一个模板工程师，编写页面模板，然后让后端负责渲染。所以在互联网早期，前端工程师这个职位可以说是不存在，通常由后端或者是美工来兼任.

## Web 2.0 前端工程师 = 软件工程师

随着 2005 年 Ajax 技术的诞生，彻底得改变了这一切，JS 脚本可以独立向服务器请求数据，拿到数据后，进行处理并更新网页，这个过程中，后端只负责提供数据，其他事情都由前端来做，就是从这个时期开始，前端逐渐变得复杂，也是从在这个时期开始，设计师和后端开发已经开始放弃前端了，开发的岗位角色悄悄地发生了变化。

---

```yaml
layout: two-cols-header
```

<style>
.slidev-layout.two-cols-header {
  grid-template-rows: 100px 1fr;
}
</style>

# 前端编程语言

::left::

前端代码主要由HTML、CSS、 JavaScript构成：

- 📝 **HTML** - 网页的核心，用于构建页面的结构
- 🎨 **CSS** - 控制网页的外观，设置页面的样式
- 🧑‍💻 **JavaScript** - 增强网页的交互，添加动效

::right::

<img src="/WX20240317-232059@2x.png" class="w-400px">

---

# 前端编程语言 - HTML

HTML(HyperText Markup Language) 全称是超文本标记语言，它不是一门编程语言，而是一种用来告知浏览器如何组织页面的标记语言。它由一系列的元素（elements）组成，这些元素可以用来包围不同部分的内容，使其以某种方式呈现或者工作。

<img src="/WX20240318-002124@2x.png" class="h-300px mx-auto">

---

# 前端编程语言 - CSS

CSS(Cascading Style Sheets) 全称是层叠样式表，它是用来样式化和排版网页的 —— 例如更改网页内容的字体、颜色、大小和间距，将内容分割成多列或者加入动画以及别的装饰型效果。它通过选择器选中上面提到的 HTML 元素，然后为选中的元素添加颜色，间距等样式。

<img src="/WX20240318-002048@2x.png" class="w-600px mx-auto">

---

# 前端编程语言 - JavaScript

JS(JavaScript) 是一种脚本编程语言，它可以在网页上实现复杂的功能，网页展现给你的不再是简单的静态信息，而是实时的内容更新——交互式的地图、2D/3D 动画、滚动播放的视频等等。它因互联网而生，紧跟着浏览器的出现而问世。随着前端的迅猛发展，它已经不像刚开始出现时那样，只是为了做了一些页面的校验，已经成了构建企业级应用的重要语言之一，是目前全球使用率最高的语言。

<img src="/JavaScript_code.png" class="w-500px mx-auto">

---

# 前端编程语言 - TypeScript

TypeScript 是微软公司开发的一种基于 JavaScript 语言的编程语言。它的目的并不是创造一种全新语言，而是增强 JavaScript 的功能，使其更适合多人合作的企业级项目。TypeScript 可以看成是 JavaScript 的超集，即它继承了后者的全部语法，所有 JavaScript 脚本都可以当作 TypeScript 脚本，此外它再增加了一些自己的语法。

- 增加了代码的可读性和可维护性，类型系统实际上是最好的文档
- 可以在编译阶段就发现大部分常见于法错误
- 增强了编辑器和 IDE 的功能，包括代码补全、接口提示、跳转到定义、重构等

<img src="/WX20240318-005220@2x.png" class="w-500px mx-auto mt-20px">

---

# 前端基础设施 - Web 浏览器

Web 浏览器可以将您带到互联网的任何角落。它从 Web 上的其他区块检索信息并将其显示在您的桌面或移动设备上。信息通过超文本传输协议进行传输，而该协议定义了文本、图像和视频在网上的传输方式。这些信息需要以一致的格式共享和显示，让世界上任何地方使用任何浏览器的人都能看到。遗憾的是，并非所有浏览器厂商都选择以相同的方式解释格式。对于用户而言，这意味着看到的网站的外观和功能可能会存在差异。

主流浏览器的市场份额：

<img src="/WX20240318-004929@2x.png" class="w-500px mx-auto">

---

# 前端基础设施 - Node.js

Node.js是一个JavaScript运行时环境，将其能力扩展到服务器端。它是建立在 Chrome 的 V8 JavaScript引擎上。
Node是一个事件驱动的非阻塞I/O模型。这意味着它是异步的，不会因为一个请求而阻塞（而是立即移动到下一个请求），这使得Node异常快速和高效。Node 使 JavaScript 成为了一种全栈语言。

<img src="/node.jsreact-application-architecture-1024x432.jpg" class="w-600px mx-auto">

---

# 前端Web应用开发框架 - React

React 是一个用于构建用户界面的 JAVASCRIPT 库，主要用于构建 UI，很多人认为 React 是 MVC 中的 V（视图）。React 拥有较高的性能，代码逻辑非常简单，越来越多的人已开始关注和使用它。

1. 声明式设计：采用声明范式，可以轻松描述应用
2. 高效：使用虚拟DOM，减少DOM的交互
3. 灵活：与已知的库或框架完好配合
4. JSX：JSX 是 JavaScript 语法的扩展，解决了很多JS的缺陷
5. 组件：通过 React 构建组件，使得代码更加容易得到复用，有利于开发大型项目
6. 单向数据流：实现了单向响应的数据流，减少了重复代码，比传统数据绑定更简单

<img src="/WX20240318-011500@2x.png" class="w-600px mx-auto">

---

# 前端客户端开发框架 - Electron

Electron是一个使用 JavaScript、HTML 和 CSS 构建桌面应用程序的框架。 通过嵌入 Chromium 和 Node.js，Electron 允许您只维护一份 JavaScript 代码，便可以创建能同时在 Windows、macOS 和 Linux 上运行的跨平台应用，而不需要原生应用开发经验。

<img src="/code-server-architecture.png" class="w-600px mx-auto">

---

# 前端应用场景

随着前端技术的发展和浏览器能力的增强，越来越多的软件会变成 Web 应用。

Atwood定律：“任何可以使用 JavaScript 来编写的应用，最终都会由 JavaScript 编写”。

<div>
  <img src="/WX20240318-012608@2x.png" class="w-600px mx-auto">
</div>

<div class="flex items-center gap-20px">
  <img src="/1_aec6BlOTGEMKmtUCdv8E0Q.png" class="w-360px mx-auto">
  <img src="/ed5839033fa34c389cd135937c8cb091~tplv-jbbdkfciu3-webp_0_0.webp" class="w-360px mx-auto">
</div>

---

<!-- ./components/ThankYou.vue -->
<div>
  <ThankYou  />
</div>

<div class="fixed left-0px bottom-20px grid grid-cols-3 gap-10px h-300px">
  <div v-click>

```html
<div class="h-full grid place-items-center">
  <div class="text-center">
    <h1 id="text">前端技术之旅告一段落</h1>
    <button
      class="h-10 px-6 font-semibold rounded-md bg-indigo-600 text-white text-sm"
      id="btn"
    >
      该做点什么呢
    </button>
  </div>
</div>
```

  </div>

  <div v-click>

```css
.grid {
  display: grid;
}
.h-10 {
  height: 2.5rem;
}
.h-full {
  height: 100%;
}
.place-items-center {
  place-items: center;
}
.rounded-md {
  border-radius: 0.375rem;
}
.bg-indigo-600 {
  --un-bg-opacity: 1;
  background-color: rgb(79 70 229 / var(--un-bg-opacity));
}
.px-6 {
  padding-left: 1.5rem;
  padding-right: 1.5rem;
}
.text-center {
  text-align: center;
}
.text-sm {
  font-size: 0.875rem;
  line-height: 1.25rem;
}
.text-white {
  --un-text-opacity: 1;
  color: rgb(255 255 255 / var(--un-text-opacity));
}
.font-semibold {
  font-weight: 600;
}
```

  </div>

  <div v-click>

```js
document.getElementById("#btn").onclick = () => {
  document.getElementById("#text").innerText = "谢谢大家，撒个花吧";
  const triangle = confetti.shapeFromPath({ path: "M0 10 L5 0 L10 10z" });
  confetti({
    shapes: [triangle],
  });
};
```

  </div>
</div>
