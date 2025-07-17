---
title: "Markdown 样式指南"
description: "这里展示了一些基本的 Markdown 语法示例，可用于在 Astro 中编写 Markdown 内容。"
pubDate: "2024 7 1"
image: /image/md.png
categories:
  - 文档
  - 示例
tags:
  - Markdown
badge: 置顶
---

这里展示了一些基本的 Markdown 语法示例，可用于在 Astro 中编写 Markdown 内容。

## 标题

HTML 的 `<h1>` 到 `<h6>` 元素代表六个级别的标题。`<h1>` 是最高级别，`<h6>` 是最低级别。

# 一级标题

## 二级标题

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题

## 段落

这是一个示例段落，展示了 Markdown 中的文本格式。在这里，我们可以自由地表达想法，组织内容结构。段落之间通过空行分隔，这是 Markdown 的基本规则之一。

第二段内容继续展示文本排版效果。通过简单的标记语法，我们可以创建结构清晰、易于阅读的文档内容。

## 图片

#### 语法

```markdown
![文本](./full/or/relative/path/of/image)
```

#### 输出

![博客占位符](/logo.png)

## 引用

引用元素表示从其他来源引用的内容，可以选择包含引用来源。

### 无来源引用

#### 语法

```markdown
> 这是一个引用示例。<br> 
> **注意**：你可以在引用中使用 *Markdown 语法*。
```

#### 输出

> 这是一个引用示例。<br> 
> **注意**：你可以在引用中使用 *Markdown 语法*。

### 带来源引用

#### 语法

```markdown
> 不要通过共享内存来通信，而要通过通信来共享内存。 <br>
> — <cite>Rob Pike</cite>
```

#### 输出

> 不要通过共享内存来通信，而要通过通信来共享内存。<br>
> — <cite>Rob Pike</cite>

[^1]: 上述引用摘自 Rob Pike 在 2015 年 11 月 18 日 Gopherfest 上的[演讲](https://www.youtube.com/watch?v=PAAkCSZUG1c)。

## 表格

#### 语法

```markdown
| 斜体 | 粗体 | 代码 |
|:-:|:-:|:-:|
| *斜体* | **粗体** | `代码` |
```

#### 输出

| 斜体 | 粗体 | 代码 |
|:-:|:-:|:-:|
| *斜体* | **粗体** | `代码` |

## 代码块

#### 语法

使用三个反引号 ``` 包裹代码块，可以在第一个反引号后指定语言名称以实现语法高亮，例如 html、javascript、css、markdown、typescript、txt、bash等。

````markdown
```cpp
#include <bits/stdc++.h>
using namespace std;
const int N = 1e5 + 5;
int n, k, a[N];
long long ans;
vector<int> v[N];
int main()
{
    scanf("%d%d", &n, &k);
    for (int i = 1; i <= n; i++)
    {
        scanf("%d", &a[i]);
        v[i % k].push_back(a[i]);
    }
    for (int i = 0; i < k; i++)
        sort(v[i].rbegin(), v[i].rend());
    for (int i = 0; i < k; i++)
    {
        for (int j = 0; j + 1 < v[i].size(); j += 2)
        {
            ans += v[i][j] + v[i][j + 1];
        }
    }
    printf("%lld\n", ans);
    return 0;
}
```
````

#### 输出

```cpp
#include <bits/stdc++.h>
using namespace std;
const int N = 1e5 + 5;
int n, k, a[N];
long long ans;
vector<int> v[N];
int main()
{
scanf("%d%d", &n, &k);
for (int i = 1; i <= n; i++)
{
scanf("%d", &a[i]);
v[i % k].push_back(a[i]);
}
for (int i = 0; i < k; i++)
sort(v[i].rbegin(), v[i].rend());
for (int i = 0; i < k; i++)
{
for (int j = 0; j + 1 < v[i].size(); j += 2)
{
ans += v[i][j] + v[i][j + 1];
}
}
printf("%lld\n", ans);
return 0;
}
```

## 列表类型

### 有序列表

#### 语法

```markdown
1. 第一项
2. 第二项
3. 第三项
```

#### 输出

1. 第一项
2. 第二项
3. 第三项

### 无序列表

#### 语法

```markdown
- 列表项
- 另一个项
- 还有一项
```

#### 输出

- 列表项
- 另一个项
- 还有一项

### 嵌套列表

#### 语法

```markdown
- 水果
  - 苹果
  - 橙子
  - 香蕉
- 乳制品
  - 牛奶
  - 奶酪
```

#### 输出

- 水果
  - 苹果
  - 橙子
  - 香蕉
- 乳制品
  - 牛奶
  - 奶酪

## 其他元素

#### 语法

```markdown
<abbr title="图形交换格式">GIF</abbr>是一种位图图像格式。

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

按下 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Delete</kbd> 结束会话。

大多数<mark>蝾螈</mark>是夜行性动物，以昆虫、蠕虫和其他小生物为食。
```

#### 输出

<abbr title="图形交换格式">GIF</abbr> 是一种位图图像格式。

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

按下 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Delete</kbd> 结束会话。

大多数<mark>蝾螈</mark>是夜行性动物，以昆虫、蠕虫和其他小生物为食。