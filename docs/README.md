# 快速开始

推荐全局安装 docsify-cli 工具,可以方便的创建在本地预览生成的文档

```bash
cnpm i  docsify-cli -g
```

# 初始化项目

如果想在项目的 ./docs 目录写文档,直接通过 init 初始化项目

```bash
docsify init ./docs
```

```javascript
var a = '23'
console.log(a)
```

# 开始写文档

初始化成功后,可以看到 ./docs 目录里写文档,直接通过 init 初始化项目

- `index.html` 入口文件

- `README.md` 会做为主页内容渲染

- `.nojekyll` 用于阻止 Github Pages 忽略掉下划线开头的文件

直接编辑 docs/README.md 就能更新文档内容,当然也可以添加更多页面

# 本地预览

通过运行 `docsify serve` 启动一个本地服务器,可以方便的实时预览效果.默认访问地址:`http://localhost:3000`

```bash
docsify serve docs
```

# Loading 提示

初始化会显示 `Loading...`内容,你可以自定义提示信息

```html
<!--index.html-->
<div id="app">加载中</div>
```

如果更改了`el`的配置,需要将该元素加上`data-app`属性

```html
<!--index.html-->
<div data-app id="main">加载中</div>
<script>
  window.$docsify = {
    el: '#main',
  }
</script>
```

# tab 练习

<!-- tabs:start -->

#### **Go**

```go

package main

func main() {
	who := "world!"
	if len(os.Args[1:]) > 0 {
who = ""
	for _, arg := range os.Args[1:] {
			who += " " + arg
	}
	}
	fmt.Println("hello", who)
}

```

#### **javascript**

```javascript
var a = 'hello'
console.log(a)
```

#### **Bash**

```bash

echo "go"
```

<!-- tabs:end -->
