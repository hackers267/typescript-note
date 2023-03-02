# 配置

## 配置路径别名

在使用`typescript`的时候，有时我们引入某个模块的时候，其路径会很长。比如我们的`src`和`tests`目录是平行的。我们要引入`src`
中的模块，在`tests`中，只能使用`../src`这样通过 *..* 来导航到`src`目录中才能方便的引用其中的模块。为了防止频繁的使用 *..*
这样的方式。我们可以引入**路径别名**。

`paths`是一系列入口的重定向。其位置相对于配置文件中的`baseUrl`。下面是两个示例：

示例1：

```json
{
  "compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "@": [
        "./src/*"
      ]
    }
  }
}
```

示例2:

```json
{
  "compilerOptions": {
    "baseUrl": "src",
    "paths": {
      "app/*": [
        "app/*"
      ],
      "config/*": [
        "config/*"
      ],
      "environment/*": [
        "environment/*"
      ],
      "shared/*": [
        "app/_shared/*"
      ],
      "helpers/*": [
        "helpers/*"
      ]
    }
  }
}
```
