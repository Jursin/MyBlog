<pre align="center">
一个使用 Frosti 主题搭建的博客 🚀 由 Astro 驱动
</pre>

<div align="center">
<img alt="Frosti Logo" src="./public/logo.png" width="280px">

[![Blog](https://img.shields.io/badge/%E7%BD%91%E7%AB%99-Blog-blue)](https://blog.jursin.top)
[![license](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/Jursin/MyBlog/blob/main/LICENSE)

</div>

## ✨ 特点

- ✅ **深色** / **浅色** 模式切换
- ✅ 极速的访问速度与优秀的 SEO
- ✅ 视图过渡动画（使用 ClientRouter）
- ✅ 搜索文章（使用 Pagefind）
- ✅ 使用 [Tailwind CSS](https://tailwindcss.com/) 与 [daisyUI](https://daisyui.com/) 构建自适应页面
- ✅ RSS 订阅支持

## ⬇️ 使用方法

1. 安装 pnpm 包管理器（如果没有安装）

   ```sh
   npm i -g pnpm
   ```

2. 克隆项目

   ```sh
   git clone https://github.com/EveSunMaple/Frosti.git Frosti
   ```

3. 进入项目文件夹

   ```sh
   cd Frosti
   ```

4. 安装依赖

   ```sh
   pnpm i
   ```

5. 调试、运行项目

   **首次运行或更新内容后**，需先执行：

   ```sh
   pnpm run search:index
   ```

   > [!tip]
   > 生成搜索索引以供开发时使用

   启动：

   ```
   pnpm run dev
   ```

## 🚀 自动更新

为了使项目与 Frosti 的最新版本保持同步，可以使用提供的更新脚本。

```sh
bash frosti.update.sh
```

该脚本将：

1.  **克隆最新版本**的 Frosti 仓库。
2.  **安全地更新**项目文件，根据 `.updateignore` 文件添加和覆盖文件。
3.  **智能地删除**官方仓库中已移除的文件，而不会影响已忽略的文件。
4.  **清理**任何残留的空文件夹和临时文件。
5.  使用 `pnpm` **安装或更新** 依赖项。
