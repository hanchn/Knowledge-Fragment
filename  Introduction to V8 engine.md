[< Back to the homepage](./README.md)

HTMX 是一种高效的 HTML 工具，它可以让你直接在 HTML 中使用 AJAX、CSS 过渡、WebSockets 和服务器发送的事件。这意味着你可以使用属性来构建现代用户界面，同时保持超文本的简单性和强大性。

HTMX 的体积很小（约 14k min.gz'd），无依赖，可扩展，兼容 IE11，并且与 React 相比，可以减少代码库大小的 67%。

与其说 HTMX 是一款前端框架，不如说它是一款 HTML 自定义属性工具库。它将很多常见的 JS 交互逻辑收敛到自定义 HTML 属性中，从而减少 JS 代码量。现代前端框架通常是状态驱动 UI，而 HTMX 的理念是过程驱动 UI（类似 jQuery 时代编写页面的方式）。

例如，你可以使用以下代码快速开始：
```html
<script src="https://unpkg.com/htmx.org@1.9.6"></script>
<button hx-post="/clicked" hx-swap="outerHTML"> Click Me </button>
```
在这个例子中，`hx-post` 和 `hx-swap` 属性告诉 HTMX：“当用户点击这个按钮时，向 /clicked 发出一个 AJAX 请求，并用 HTML 响应替换整个按钮”。

HTMX 是 intercooler.js 的后继者。如果你想了解更多关于 HTMX 的信息，可以查阅其[官方文档](^1^)。

HTMX 提供了一些有用的 API 方法，主要用于扩展开发或处理事件。以下是一些示例：

- `htmx.addClass()`：此方法将类添加到给定元素。例如，`htmx.addClass(htmx.find('#demo'), 'myClass');` 将 'myClass' 类添加到 id 为 'demo' 的元素。
- `htmx.ajax()`：发出 htmx 风格的 AJAX 请求。例如，`htmx.ajax('GET', '/example', '#myDiv')` 向 /example 发出 GET 请求，并将响应 HTML 放入 #myDiv。
- `htmx.closest()`：在给定元素的父级中找到最接近的匹配元素。例如，`htmx.closest(htmx.find('#demo'), 'div');` 找到 id 为 'demo' 的元素的最接近的 div。
- `htmx.config`：保存 htmx 在运行时使用的配置。

HTMX 还支持通过扩展进行形态转换。此外，HTMX 扩展并概括了 HTML 作为超文本的核心思想，直接在语言中打开了更多可能性：现在任何元素，而不仅仅是锚点和表单，都可以发出 HTTP 请求。现在任何事件，而不仅仅是点击或表单提交，都可以触发请求。

HTMX 是一种简单、高效且强大的工具，可以帮助开发者更好地创建现代化的用户界面。