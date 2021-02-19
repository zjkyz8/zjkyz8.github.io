### 风格指南
## 谷歌风格指南
每个重要的开源项目都会一套关于如何编写本项目代码的约定（有时是随意的）。如果一个大型代码库中的所有代码保持统一的风格，那么这个代码库中的代码是非常容易理解的。

“风格”涵盖很多方面，从“使用驼峰字为变量命名”到“禁止使用全局变量”再到“禁止使用异常”。本项目主要介绍谷歌代码使用的风格指引。如果你正在修改一个源自谷歌的项目，那么本文档将帮助你理解该项目所遵循的风格指引。

本项目包含了[C++风格指南](https://google.github.io/styleguide/cppguide.html)，[C#风格指南](https://google.github.io/styleguide/csharp-style.html)，[Swift风格指南](https://google.github.io/swift/)，[Objective-C风格指南](https://google.github.io/styleguide/objcguide.html)，[Java风格指南](https://google.github.io/styleguide/javaguide.html)，[Python风格指南](https://zjkyz8.github.io/chinese/google-eng/styleguide/python)，[R风格指南](https://google.github.io/styleguide/Rguide.html)，[Shell风格指南](https://google.github.io/styleguide/shellguide.html)，[HTML/CSS风格指南](https://google.github.io/styleguide/htmlcssguide.html)，[JavaScript风格指南](https://google.github.io/styleguide/jsguide.html)，[TypeScript风格指南](https://google.github.io/styleguide/tsguide.html)，[AngularJS风格指南](https://google.github.io/styleguide/angularjs-google-style.html)，[Common Lisp风格指南](https://google.github.io/styleguide/lispguide.xml)，以及[VimScript风格指南](https://google.github.io/styleguide/vimscriptguide.xml)。同时,本项目包含一个辅助风格指引落地的工具[cpplint](https://github.com/google/styleguide/tree/gh-pages/cpplint)和一个实现谷歌风格的Emacs配置文件[google-c-style.el](https://raw.githubusercontent.com/google/styleguide/gh-pages/google-c-style.el)。

如果你的项目需要创建一个新的XML文档格式，那么可以使用[XML文档格式风格指南](https://google.github.io/styleguide/xmlstyle.html)。处理实际的风格规则外，此文档中还包括一些定义私有格式还是使用公共格式的建议，XML示例文档格式化建议、以及使用元素还是使用属性的建议。

本项目中包含的风格指南使用CC-By 3.0许可，具体请参阅 https://creativecommons.org/licenses/by/3.0/

以下的谷歌风格指南不包含在本项目中：[Go代码审核备注](https://golang.org/wiki/CodeReviewComments)与[高效Dart](https://www.dartlang.org/guides/language/effective-dart)。