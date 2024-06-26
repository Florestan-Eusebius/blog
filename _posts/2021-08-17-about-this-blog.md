---
layout: article
title: 关于这个博客
tags: 
- 工具
---

之前搭的博客由于太久远, 维护得有些混乱, 干脆推倒重来. 内容的组织逻辑也有变化. <!--more-->

## 博客的搭建

系统: Windows 10

### 建立 Git 仓库

建立名称为 `<username>.github.io` 的仓库.

在本地创建 `MyBlog` 目录, 将远程仓库与此关联.

```bash
git init
git remote add origin git@github.com:<username>/<repository name>.git
```

### 安装 Ruby, RubyGems, Jekyll 和 Bundler

参考文档 [Jekyll Docs](https://jekyllrb.com/docs/installation/)

在 [Downloads (rubyinstaller.org)](https://rubyinstaller.org/downloads/) 安装 `Ruby+Devkit`. 运行安装文件将其安装到 `C:/`. 

运行

``` bash
gem install jekyll bundler
```

### 使用 Jekyll 建立博客

在博客目录中 `jekyll new .` 可以建立一个简单的新博客. 我这里直接将 TeXt 主题的文件复制到了本地. 参考[快速开始 - TeXt Theme (tianqi.name)](https://tianqi.name/jekyll-TeXt-theme/docs/zh/quick-start).

使用如下命令预览

```bash
bundle exec jekyll server
```

报错

```bash
cannot load such file -- webrick
```

运行 `bundle add webrick` 安装. 再次尝试预览, 成功!

## 常用维护方式

在 `_posts` 目录中按照已有文件的格式创建新文件即可. 在使用

```bash
bundle exec jekyll server
```

预览的过程中, 浏览器中内容可即时刷新. 此时已生成对应文件. 因此直接 add - commit - push 即可完成部署.

## 内容

博客里文章主要分三种, 一是随笔和文艺创作, 二是一些技术向的操作记录, 三是科普或趣味向的学术短文. 考虑到 markdown 对公式的支持还是非常有限, 主要的学术内容放在 Notes 版块里 (见标题栏), 以 PDF 的形式呈现.

2020 年 1 月 10 日初搭博客的时候，我是这么写的

> 很早就想給自己弄一個博客。記得上小學時（已經是十幾年前的事了），老師教我們申請博客。我當時申請了一個——坐在爸媽臥室的椅子上，面對着4G硬盤的長屁股聯想電腦，自己搗鼓了很久，把電腦整得一陣一陣地吹風。興奮地給媽媽看，“你還能得很，會弄博客了！”，媽媽就又回到客廳看電視了，我也就跟了過去。當時還是覺得坐在媽媽懷裏看電視連續劇更吸引我，卻實在沒有表達的能力和欲望，後來就連博客帳號也不記得了。上了大學，表達欲開始膨脹，想申請一個博客，看了一圈，國內這些運營商的審美實在讓人不敢恭維，於是就網上找教程自己搭。沒錢，也不想花錢買域名，這個 github.io 就剛好，每次看到都誘惑我走向 CS 的康莊大道。
>
> 博客寫什麼？一是所謂「乾貨」。我是學物理的，數學也學一點，平時有什麼思考，可以寫在這裏。這是本行，要保證專業水準的。二是摻些水的半乾貨，業餘涉獵計算機、音樂、文學等等，有所得，輒書於此，於是這就僅僅是個人的體驗與想法，不保證專業性。三是隨筆，寫一些日常的見聞和思考，儘量寫些美好的東西，有時候編一兩個小故事，也放在這裏。
> 
> 一般而言，有表達，就有接收，有作者，就有讀者。但我實在也不指望我這滿屏荒唐言能有人閱讀。我寫日記，很隨意地寫，自然也有很多見不得人的言語。但除此之外，有時還想寫一些稍有打磨或者稍有知識含量的文字，放在這裏就正合適。這裏的文字只是日記的升級版，給自己搭一個精神家園，留一點回憶的素材。後之視今，亦猶今之視昔——或許將來看到今天的生活點滴和技術載體，就像現在看十幾年前一樣，在嘆惋中狐疑地欣賞着別具風味的落後，反覆品味那小題大做的焦慮和幸福。
>
> 聽起來是很有趣罷。

## 迁移

2022 年 1 月 16 日更新。

由于所有文件均在 GitHub 上，迁移只需克隆即可。Mac 上环境配置需要注意使用 Homebrew 下载新的 ruby，具体方法见[这篇文章](https://zhuanlan.zhihu.com/p/350462079)。