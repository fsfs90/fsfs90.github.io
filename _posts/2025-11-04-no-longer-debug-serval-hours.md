---
title: 久违的超长时间的 debug
categories: [comment]
comments: true
---

有了 ai 编程以后，我解决我业余项目的 bug 基本上就是 2、3 轮对话的事儿。没有了之前为了 debug，超长时间的查资料、重复试，一下几个小时持续。当然我遇到的 bug 一般是基础不牢导致的，debug 结果出来以后会知道是很小一个问题。

docker-compose 原来也需要 build，up down 不会重新 build，所以修改代码的修改不会生效。这个 bug 几轮对话改好了。把我的 simple rss reader 项目放到 docker 里运行，只在 codex 上输入“生成 docker-compose.yml，试这个项目在 docker 中运行，和我讨论细节实现”。然后确认了几个问题，生成了 docker-compose 文件，运行时的错误复制粘贴到 chatgpt，精准定位到了问题，是 npm run build 的错误。还有缺少 typescript 的依赖。之后 --dev install 之后，又出错，又贴到 chatgpt，又精准地定位问题为需从 dev dependency 变成 dependency。这放到过去，肯定是比现在要更大费周章。