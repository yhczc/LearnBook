# HTML 段落
HTML 可以将文档分割为若干段落
## HTML 段落
段落是通过` <p>` 标签定义的。
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="MLmzpW" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 段落">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/MLmzpW/">
  HTML 段落</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
>**注意：**浏览器会自动地在段落的前后添加空行。（`</p>` 是块级元素）

## 不要忘记结束标签
即使忘了使用结束标签，大多数浏览器也会正确地将 HTML 显示出来：

上面的例子在大多数浏览器中都没问题，但不要依赖这种做法。忘记使用结束标签会产生意想不到的结果和错误。
>**注释:** 在未来的 HTML 版本中，不允许省略结束标签。

## HTML 折行
如果您希望在不产生一个新段落的情况下进行换行（新行），请使用 `<br /> `标签：
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="LqyvYd" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 折行">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/LqyvYd/">
  HTML 折行</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
`<br />` 元素是一个空的 HTML 元素。由于关闭标签没有任何意义，因此它没有结束标签。

##  ` <br>` 还是 `<br />`
您也许发现 `<br>` 与` <br />` 很相似。
在 XHTML、XML 以及未来的 HTML 版本中，不允许使用没有结束标签（闭合标签）的 HTML 元素。
即使 `<br>` 在所有浏览器中的显示都没有问题，使用` <br />` 也是更长远的保障。
## HTML 输出 - 有用的提示
我们无法确定 HTML 被显示的确切效果。屏幕的大小，以及对窗口的调整都可能导致不同的结果。
对于 HTML，您无法通过在 HTML 代码中添加额外的空格或换行来改变输出的效果。
当显示页面时，浏览器会移除**源代码中**多余的空格和空行。所有连续的空格或空行都会被算作一个空格。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="aXWxOV" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 输出 - 有用的提示">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/aXWxOV/">
  HTML 输出 - 有用的提示</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
（这个例子演示了一些 HTML 格式化方面的问题）
