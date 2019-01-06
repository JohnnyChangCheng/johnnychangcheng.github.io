---
layout: post
title: Jekyll 架站 at Github
tags: [web]
---
本業不是Web工程師,要用GitHub的空間架出一個簡單的Blog也是煞費苦心,於是留下這篇文章紀錄一下坑坑洞洞 <br/>
作業環境 : Ubuntu 18.04 <br/>
前置技能 : 基礎的Command Line 技能跟Git 知識 <br/>
在看過網路上教學文章,有關在github上架站的套件大多數都推Jekyll,尤其github官方就幫Jekyll寫了一篇教學文 <br/>
網址如下:[Github Offical](https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/)  <br/>
Jekyll : 在Ubuntu上可以直接用sudo apt-get install jekyll <br/>
如果要用Jekyll最陽春的功能步驟如下 :<br/>
 - 1. 在Github開一個Repository 並且名稱要叫 ${帳號的名字}.github.io 不然會有很多坑等著你踩@@ <br/>
![My github screenshot](/img/gitpage.jpg)
 - 2. git clone 個人的Repository 並 $ jekyll johnnychangcheng.github.io (跟你git repository的Name有關)<br/>
 - 3. $ jekyll serve  <br/>
 - 4. 在 任一瀏覽器輸入 http://127.0.0.1:4000/ 就可以看到jekyll最陽春的畫面了!恭喜你第一步完成了 <br/>
 - 5. 接著把這個Repository砍掉,因為我們要進入正題了,用第三方作者提供的jekyll來架blog <br/>
      除非是前端工程師,不然還是乖乖用第三方的素材來架站比較方便
