---
layout: post
title: JAMStack Getting Started Guide with Jekyll and Netlify
author: dan_urbanowicz
date: '2019-07-30 20:06:54'
intro_paragraph: >-
  This is a guide to using the latest technology (the JAMStack), the some of the
  best, most renowned tools (Netlify and Jekyll) to create a blazing fast and
  beautiful blog — for free. It uses Github for storage, and Netlify CMS for
  easy content management. (The only cost you will incur later, when you want,
  is a domain name. Everything else is free.)


  I wanted to figure out how to do this, so I decided to take notes as I did it,
  and share them as I go along.


  # Let's see how to do it.


  In this guide...


  The tools you need to build your first JAMStack Website — Jekyll, Netlify and
  Netlify CMS (these are two separate things)


  A guide to getting your website launched and your first blog post working


  Quick introduction to JAMStack and why to use it


  ## Why use Jekyll and Netlify


  Things you need to get started


  Github account (free). Github is a place where people can store code for free.
  It's used by huge companies and individual developers to share code. It's also
  used as the place for "source code" for websites. Yes, this means the "source
  code" for your website is public, unless you pay for a private Github account
  ($7/month). This shouldn't be a problem though because the source code for
  most websites is public. The only caveat is if you have such an advanced theme
  you want to keep it private — in which case, it's unlikely you'd be reading
  this introductory guide.


  Netlify account (free). Netlify is this awesome free service that lets you
  publish static websites for free. It has some advanced stuff you pay for, but
  you don't need to.


  Domain name (optional, from $5/year). If you want to publish your website to a
  real domain — and take advantage of Netlify's SSL service — you need your own
  domain. This can be a whole new one, or a subdomain (like test.hooshmand.net).


  Need a domain? Get $2 off at Hover.com (I get $2 too). I like Hover because
  their customer support policy is "a human on the phone in one ring", and it
  has been that way for the last eight years.


  Let's get started and build your Jekyll/Netlify website, and afterwards talk
  about why this is a good idea.


  Deploy a template to Github


  The best way to get started is to deploy a template to Github. After that, you
  can go around customising the content and the template to make it awesome.


  Here's the base template for Netlify and CMS. Go into that site, and click
  "Deploy to Netlify".


  Start your Jekyll/Netlify site with the "Deploy to netlify" button


  Click on "Connect to Github" on the next page.


  Give your repository a name. I'm calling it "motorcycle-forum-deals" beacuse
  that's the website I'm going to create.


  Your website will start deploying, which means files are copying over and it's
  getting set up. After about a minute, it'll be live and look like this.


  Your Jekyll website will deploy soon


  It gets given a weird name, but you can poke around in places like "site
  settings" to modify that. I changed mine to "motorcycle-forum-deals".


  Create a new post so it shows up on your blog.


  It's a good idea to create a new post first, just so you know what you're
  getting into.


  Go to your admin panel. This is your domain with /admin on the end. So mine
  became https://motorcycle-forum-deals.netlify.com/admin.


  * You click on Log in with netlify and... oh wait, what's your password??

  * The Log in window for your new Netlify CMS blog.

  * You'll have received a few emails. One of them is "You have been invited".
  Accept the invite!


  Create the post you want to make. Get a feel for the editor this way. It's not
  elegant and beautiful, like Ghost's editor or a Medium blog, but it's
  functional and easy to use.


  ```

  The Netlify CMS interface. After filling out the various fields, you have to
  hit "Save", set the status to "Ready", and then hit "Publish".

  ```


  Note: You probably won't see this live yet. Why not? And why a bunch of other
  thigns?


  1. A few questions after creating your new post in Netlify CMS

  2. You can answer the questions below by poking around in your Github
  repository.

  3. It is basically like a folder of fiels, and isn't hard to use.


  Why isn't my post live on my blog?


  The main reason your Jekyll/Github/Netlify isn't live: your time zone is
  different to Github's time zone, so your post is in the "future". For example,
  I'm currently in GMT+3. I published a post, which ended up being timestamped
  30 June 2019 11am. It's not that time in my server's time zone yet, so it
  didn't get published.


  To fix this, edit _config.yml and set future: true.


  This killed me for a while until I found the right way to google the answer!


  Where does your Netlify CMS post and data go?


  Netlify CMS is basically a pretty interface that lets you upload images and
  markdown posts to your Github repository. It's all there in the public, just
  unformatted. Yes, this means someone could clone your whole website if your
  repository is public.


  If you go log into Github, you can find:


  your posts under _posts


  your images under assets/img/uploads


  Why did I have to choose some other person as the "author"?


  To change the list of authors, you edit the /admin/config.yml file.


  options:


  ```

  - { label: "Dana Hooshmand", value: "dana_hooshmand" }

  ```


  ```

  - { label: "Admin", value: "admin" }

  ```


  You can customise the list of authors in ./_data/authors.yml. After this, your
  new authors will be available in new (and old) blog posts on Netlify CMS.


  Also create the metadata for your authors, so you can feature them in posts
  (this is less critical). This is done in the authors.yml data file under
  /_data.


  `admin:`


  `\    name: Motorcycle Forum Deals`


  `\    email: info@motorcycle-forum-deals.netlify.com`


  `\    web: https://motorcycle-forum-deals.netlify.com`


  `dana_hooshmand`


  `\    name: Dana Hooshmand`


  `\    email: spam@hooshmand.net`


  `\    web: https://hooshmand.net`


  How I change the name of the blog?


  Edit info like your blog's name in _config.yml. There's some other baseline
  config to do there too!


  Now your blog should be working.


  Here's our first post, live.


  Add a new theme to your new and functional Jekyll blog!


  One of the coolest things about Jekyll is that it's themeable. You can install
  ruby gem themes, or you can just modify the css and template pages yourself.


  It's a topic on its own though, so I'll make a separate post for that in
  detail.


  ![test arl](/assets/img/uploads/ed488a1c557e97b667adf67dfa5239e7.jpg "Wow
  Test")


  But in essence there are two kinds of themes for a Jekyll blog:


  A custom-built theme, where you edit all the templates and CSS yourself. Of
  course you can do this.


  A theme "gem" built by someone else (or you). These are much easier to updaet,
  but provide less flexibilty.


  Here's a good guide to building your first theme gem.


  Why build a website using the JAMStack?


  This is one of the easiest ways to be at the very edge of the most modern
  forms of web publishing: the JAMStack.


  The JAMStack is a complicated way of saying "let's split up what the
  designers, engineers, and content writers all do." It's an acronym but it's
  not a useful one to explain... it's Javascript, APIs and Markup, and I have to
  Google it every time, and wonder "why did they call it that??"


  Anyway the JAMStack lets you split out what people do, by letting:


  ![](/assets/img/uploads/screenshot-editor.jpg)


  Designers modify theme files, without modifying any posts or the code


  Engineers create blazing-fast deployment systems (deploying directly to the
  "edge" of the internet, so there's no server somewhere)


  Content producers just write posts and upload photos and don't care where it
  goes.


  You can also swap bits out, like use a different deployment system, or move
  your posts to a different place. It doesn't affect the website.


  The end result, by the way, is that the website is incredibly fast. The
  JAMStack systems all take information and spit out "static sites" that are
  pure HTML. This is the fastest way to serve a website because it means you
  don't have to fetch information from a database.


  Why build a Jekyll/Netlify CMS/Github/Netlify blog?


  Choosing the elements of the JAMStack site you want to build is very hard —
  although some of it is easier. This is why I suggested these components:


  Github: This is the easiest part to suggest. Github is a massive company with
  an amazing free service, hosting your code for free. They even have their own
  website deployment service, Github Pages. There are sooooo many people who
  host their websites on Github in public or private repositories that it makes
  for an obvious choice. There are some alternatives, like Bitbucket, but they
  don't work as well with Netlify.


  <https://www.youtube.com/watch?v=ZqJ57XRzE40>


  Netlify: Free hosting at the edge of the internet. They charge for some
  value-added features, like forms, but you don't need those. The best
  alternative is Amazon Cloudfront, which is "nearly free" (will cost you
  pennies a month). However, it does need a credit card, and is way harder to
  set up.


  Netlify CMS: It's hard choosing a CMS. The main criteria I had was that I
  wanted all the content stored on the Github account. Markdown in one folder,
  photos in another. This means you don't even need the CMS — you can just go in
  there and edit the files! Most other CMS are much more complicated than this,
  like the Ghost CMS system, or Contentful, which is really popular but $40 a
  month.


  Jekyll for a static site generator: This is the hardest decision. There are
  many static site generators, and they're all great. My main criteria was: open
  source, popular, well-supported. Alternatives are Next.js, Hugo, Gatsby, Hexo,
  and then a bunch of other ones. Jekyll has the second-most stars on Github,
  after Next.js — which doesn't have a "Deploy to Netlify" function. I'll
  produce guides for the other ones at a later stage.


  What's next?
---

