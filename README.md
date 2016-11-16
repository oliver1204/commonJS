# CommonJS规范
   CommonJS 规范是为了解决 JavaScript 的`作用域`问题而定义的模块形式，可以使每个模块它自身的命名空间中执行。该规范的主要内容是，模块必须通过
module.exports 导出对外的变量或接口，通过 require() 来导入其他模块的输出到当前模块作用域中。

   CommonJS 是同步加载模块，但其实也有浏览器端的实现，其原理是现将所有模块都定义好并通过 id 索引，这样就可以方便的在浏览器环境中解析了，可以参考
require1k 和 tiny-browser-require 的源码来理解其解析（resolve）的过程。

ps: 在ES6之前，最主要的有CommonJS和AMD两种模块加载方案。前者用于服务器，后者用于浏览器。ES6在语言规格的层面上，实现了模块功能，而且实现得相当简单，完全可以取代现有的CommonJS和AMD规范，成为浏览器和服务器通用的模块解决方案.
