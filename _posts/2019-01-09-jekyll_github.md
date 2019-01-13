---
layout: post
title: Jekyll 架站 at Github
tags: [web,Backend]
---
本業不是Web工程師,要用GitHub的空間架出一個簡單的Blog也是煞費苦心,於是留下這篇文章紀錄一下坑坑洞洞 <br/>
作業環境 : Ubuntu 18.04 <br/>
前置技能 : 基礎的Command Line 技能跟Git 知識 <br/>
在看過網路上教學文章,有關在github上架站的套件大多數都推Jekyll,尤其github官方就幫Jekyll寫了一篇教學文 <br/>
網址如下:[Github Offical](https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/)  <br/>
Jekyll : 在Ubuntu上可以直接用sudo apt-get install jekyll <br/>
如果要用Jekyll最陽春的功能步驟如下 :<br/>
 - 在Github開一個Repository 並且名稱要叫 ${帳號的名字}.github.io 不然會有很多坑等著你踩@@ <br/>
![My github screenshot](/img/gitpage.jpg)
 - git clone 個人的Repository 並 $ jekyll johnnychangcheng.github.io (跟你git repository的Name有關)<br/>
 - $ jekyll serve  <br/>
 - 在 任一瀏覽器輸入 http://127.0.0.1:4000/ 就可以看到jekyll最陽春的畫面了!恭喜你第一步完成了 <br/>
 - 接著把這個Repository砍掉,因為我們要進入正題了,用第三方作者提供的jekyll來架blog <br/>
      除非是前端工程師,不然還是乖乖用第三方的素材來架站比較方便
 - 如下方的Github [Jkelly Theme](https://github.com/daattali/beautiful-jekyll/)  <br/>

### 1. Fork this repository

(Assuming you are on this page and logged into GitHub) Fork this repository by clicking the *Fork* button on the top right corner. Forking means that you now copied this whole project and all the files into your account.

### 2. Rename the repository to `<yourusername>.github.io`

This will create a GitHub User page ready with the **Beautiful Jekyll** template that will be available at `https://<yourusername>.github.io` within a couple minutes.  To do this, click on *Settings* at the top (the cog icon) and there you'll have an option to rename.

### 3. Customize your website settings

Edit the `_config.yml` file to change all the settings to reflect your site. To edit the file, click on it and then click on the pencil icon (watch the video tutorial above if you're confused).  The settings in the file are fairly self-explanatory and I added comments inside the file to help you further. Any line that begins with a pound sign (`#`) is a comment, and the rest of the lines are actual settings.

Another way to edit the config file (or any other file) is to use [prose.io](https://prose.io/), which is just a simple interface to allow you to more intuitively edit files or add new files to your project.

After you save your changes to the config file (by clicking on *Commit changes* as the video tutorial shows), your website should be ready in a minute or two at `https://<yourusername>.github.io`. Every time you make a change to any file, your website will get rebuilt and should be updated in about a minute or so.

You can now visit your shiny new website, which will be seeded with several sample blog posts and a couple other pages. Your website is at `https://<yourusername>.github.io` (replace `<yourusername>` with your user name). Do not add `www` to the URL - it will not work!

**Note:** The video above goes through the setup for a user with username `daattalitest`. I only edited one setting in the `_config.yml` file in the video, but **you should actually go through the rest of the settings as well. Don't be lazy, go through all the settings :)**

## Add your own content

To add pages to your site, you can either write a markdown file (`.md`) or you can write an HTML file directly.  It is much easier to write markdown than HTML, so I suggest you do that (use the [tutorial I mentioned above](https://markdowntutorial.com/) if you need to learn markdown). You can look at some files on this site to get an idea of how to write markdown. To look at existing files, click on any file that ends in `.md`, for example [`aboutme.md`](./aboutme.md). On the next page you can see some nicely formatted text (there is a word in bold, a link, bullet points), and if you click on the pencil icon to edit the file, you will see the markdown that generated the pretty text. Very easy!

In contrast, look at [`index.html`](./index.html). That's how your write HTML - not as pretty. So stick with markdown if you don't know HTML.

Any file that you add inside the [`_posts`](./_posts) directory will be treated as a blog entry.  You can look at the existing files there to get an idea of how to write blog posts.  After you successfully add your own post, you can delete the existing files inside [`_posts`](./_posts) to remove the sample posts, as those are just demo posts to help you learn.

As mentioned previously, you can use [prose.io](https://prose.io/) to add or edit files instead of doing it directly on GitHub, it can be a little easier that way.

## Last important thing: YAML front matter ("parameters" for a page)

In order to have your new pages use this template and not just be plain pages, you need to add [YAML front matter](https://jekyllrb.com/docs/front-matter/) to the top of each page. This is where you'll give each page some parameters that I made available, such as a title and subtitle. I'll go into more detail about what parameters are available later. If you don't want to use any parameters on your new page (this also means having no title), then use the empty YAML front matter:

### 總結用第三方的GithubTheme就簡化了許多繁雜的步驟