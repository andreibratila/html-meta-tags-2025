Copied from: 
https://gist.github.com/lancejpollard/1978404
https://github.com/kevinSuttle/html-meta-tags 

## Basic HTML Meta Tags

``` html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="150 words"/>
<meta name=generator content="Frontweaver 8.2">
<meta name="author" content="name name name">
<meta name="referrer" content="strict-origin-when-cross-origin">
<!-- 
  Available directives:
  - index/noindex: Allow/prevent page indexing
  - follow/nofollow: Allow/prevent link crawling
  - noimageindex: Prevent image indexing
  - none: Shorthand for noindex,nofollow
-->
<meta name="robots" content="index,follow" />
<!-- 
  Available directives:
  - index/noindex: Allow/prevent page indexing
  - follow/nofollow: Allow/prevent link crawling
  - noimageindex: Prevent image indexing
  - none: Shorthand for noindex,nofollow
-->
- only webapp or pwa 
<meta name="application-name" content="my app">
```

## OpenGraph Meta Tags

``` html
<meta name="og:title" content="The Rock"/>
<meta name="og:type" content="movie"/>
<meta name="og:url" content="http://www.imdb.com/title/tt0117500/"/>
<meta name="og:image" content="http://ia.media-imdb.com/rock.jpg"/>
<meta name="og:site_name" content="IMDb"/>
<meta name="og:description" content="A group of U.S. Marines, under command of..."/>

<meta name="fb:page_id" content="43929265776" />

<meta name="og:email" content="me@example.com"/>
<meta name="og:phone_number" content="650-123-4567"/>
<meta name="og:fax_number" content="+1-415-123-4567"/>

<meta name="og:latitude" content="37.416343"/>
<meta name="og:longitude" content="-122.153013"/>
<meta name="og:street-address" content="1601 S California Ave"/>
<meta name="og:locality" content="Palo Alto"/>
<meta name="og:region" content="CA"/>
<meta name="og:postal-code" content="94304"/>
<meta name="og:country-name" content="USA"/>

<meta property="og:type" content="game.achievement"/>
<meta property="og:points" content="POINTS_FOR_ACHIEVEMENT"/>

<meta property="og:video" content="http://example.com/awesome.swf" />
<meta property="og:video:height" content="640" />
<meta property="og:video:width" content="385" />
<meta property="og:video:type" content="application/x-shockwave-flash" />
<meta property="og:video" content="http://example.com/html5.mp4" />
<meta property="og:video:type" content="video/mp4" />
<meta property="og:video" content="http://example.com/fallback.vid" />
<meta property="og:video:type" content="text/html" />

<meta property="og:audio" content="http://example.com/amazing.mp3" />
<meta property="og:audio:title" content="Amazing Song" />
<meta property="og:audio:artist" content="Amazing Band" />
<meta property="og:audio:album" content="Amazing Album" />
<meta property="og:audio:type" content="application/mp3" />
```

## Create Custom Meta Tags

Use custom meta tags to store data that you need in javascript, instead of hard-coding that data into your javascript.  I store my Google Analytics code in meta tags.  Here's some examples:

``` html
<meta name="google-analytics" content="1-AHFKALJ"/>
<meta name="disqus" content="abcdefg"/>
<meta name="uservoice" content="asdfasdf"/>
<meta name="mixpanel" content="asdfasdf"/>
```

## Company/Service Meta Tags

#### ClaimID

``` html
<meta name="microid" content="mailto+http:sha1:e6058ed7fca4a1921cq91d7f1f3b8736cd3cc1g7" />
```
    
#### Apple Meta Tags

``` html
<meta name="apple-mobile-web-app-capable" content="yes">
<meta content="yes" name="apple-touch-fullscreen" />
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="format-detection" content="telephone=no">
<meta name="viewport" content="width = 320, initial-scale = 2.3, user-scalable = no">
```

#### Internet Explorer Meta Tags

``` html
<meta http-equiv="Page-Enter" content="RevealTrans(Duration=2.0,Transition=2)" />
<meta http-equiv="Page-Exit" content="RevealTrans(Duration=3.0,Transition=12)" />
<meta name="mssmarttagspreventparsing" content="true">
<meta http-equiv="X-UA-Compatible" content="chrome=1">
<meta name="msapplication-starturl" content="http://blog.reybango.com/about/"/>
<meta name="msapplication-window" content="width=800;height=600"/>
<meta name="msapplication-navbutton-color" content="red"/>
<meta name="application-name" content="Rey Bango Front-end Developer"/>
<meta name="msapplication-tooltip" content="Launch Rey Bango's Blog"/>
<meta name="msapplication-task" content="name=About;action-uri=/about/;icon-uri=/images/about.ico" />
<meta name="msapplication-task" content="name=The Big List;action-uri=/the-big-list-of-javascript-css-and-html-development-tools-libraries-projects-and-books/;icon-uri=/images/list_links.ico" />
<meta name="msapplication-task" content="name=jQuery Posts;action-uri=/category/jquery/;icon-uri=/images/jquery.ico" />
<meta name="msapplication-task" content="name=Start Developing;action-uri=/category/javascript/;icon-uri=/images/script.ico" />
<link rel="shortcut icon" href="/images/favicon.ico" />
```

#### TweetMeme Meta Tags

``` html
<meta name="tweetmeme-title" content="Retweet Button Explained" />
```

#### Blog Catalog Meta Tags

``` html
<meta name="blogcatalog" />
```

#### Rails Meta Tags

``` html
<meta name="csrf-param" content="authenticity_token"/>
<meta name="csrf-token" content="/bZVwvomkAnwAI1Qd37lFeewvpOIiackk9121fFwWwc="/>
```

#### Apple Tags

``` html
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="format-detection" content="telephone=no">
<meta name= "viewport" content = "width = 320, initial-scale = 2.3, user-scalable = no">
<meta name= "viewport" content = "width = device-width">
<meta name = "viewport" content = "initial-scale = 1.0">
<meta name = "viewport" content = "initial-scale = 2.3, user-scalable = no">
<link rel="apple-touch-icon" href="touch-icon-iphone.png" />
<link rel="apple-touch-icon" sizes="72x72" href="touch-icon-ipad.png" />
<link rel="apple-touch-icon" sizes="114x114" href="touch-icon-iphone4.png" />
<link rel="apple-touch-startup-image" href="/startup.png">

<link rel="apple-touch-icon" type="image/png" href="/apple-touch-icon.png" />
```
    
## HTML Link Tags

``` html
<link rel="alternate" type="application/rss+xml" title="RSS" href="http://feeds.feedburner.com/martini" />
<link rel="shortcut icon" type="image/ico" href="/favicon.ico" />
<link rel="fluid-icon" type="image/png" href="/fluid-icon.png" />
<link rel="me" type="text/html" href="http://google.com/profiles/thenextweb"/>
<link rel='shortlink' href='http://blog.unto.net/?p=353' />
<link rel='archives' title='May 2003' href='http://blog.unto.net/2003/05/' />
<link rel='index' title='DeWitt Clinton' href='http://blog.unto.net/' />
<link rel='start' title='Pattern Recognition 1' href='http://blog.unto.net/photos/pattern_recognition_1_about/' />
<link rel='prev' title='OpenSearch and OpenID?  A sure way to get my attention.' href='http://blog.unto.net/opensearch/opensearch-and-openid-a-sure-way-to-get-my-attention/' />
<link rel='next' title='Not blog' href='http://blog.unto.net/meta/not-blog/' />
<link rel="search" href="/search.xml" type="application/opensearchdescription+xml" title="Viatropos" />

<link rel="self" type="application/atom+xml" href="http://www.syfyportal.com/atomFeed.php?page=3"/>
<link rel="first" href="http://www.syfyportal.com/atomFeed.php"/>
<link rel="next" href="http://www.syfyportal.com/atomFeed.php?page=4"/>
<link rel="previous" href="http://www.syfyportal.com/atomFeed.php?page=2"/>
<link rel="last" href="http://www.syfyportal.com/atomFeed.php?page=147"/>

<link rel='shortlink' href='http://smallbiztrends.com/?p=43625' />
<link rel="canonical" href="http://smallbiztrends.com/2010/06/9-things-to-do-before-entering-social-media.html" />
<link rel="EditURI" type="application/rsd+xml" title="RSD" href="http://smallbiztrends.com/xmlrpc.php?rsd" />
<link rel="pingback" href="http://smallbiztrends.com/xmlrpc.php" />
<link media="only screen and (max-device-width: 480px)" href="http://wordpress.org/style/iphone.css" type="text/css" rel="stylesheet" />
```
## Redundant 

### `<meta http-equiv="x-dns-prefetch-control" content="on">`
- **Why Redundant?**:  
  Modern browsers (Chrome/Firefox/Safari) enable DNS prefetching by default.
- **Modern Alternative**:  
  ```html
  <!-- More effective resource hint -->
  <link rel="preconnect" href="https://cdn.example.com">
  <!-- For critical resources -->
  <link rel="preload" href="font.woff2" as="font" type="font/woff2" crossorigin>

  
## Deprecated or nearly deprecated

### `<meta name="copyright" content="">`
- **Reason**: Intended to declare copyright ownership.
- **Status**: **Redundant** — Valid in HTML5 but ineffective for SEO or legal protection.
- **Modern alternative**:
  - Visible copyright notice in the footer (e.g., `© 2023 Company Name`).
  - Link to a **`/copyright`** page or use **Schema.org `copyrightNotice`** in structured data.



### `<meta name="keywords" content="word1, word2, word3">`
- **Reason**: Originally helped search engines understand page content via keyword lists.
- **Status**: **Useless** - Google officially stopped using it in 2009 due to rampant spam abuse.
- **Modern alternative**: Focus on natural keyword placement in content and structured data (Schema.org).

### `<meta itemprop="[property]" content="[value]">`
- **Purpose**: Part of Schema.org microdata syntax for structured data markup (2011-2015 era).
- **Status**: **Legacy** - Still parsed but replaced by JSON-LD as the modern standard.
- **Replacement**: 
  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "[TYPE]",
    "[PROPERTY]": "[VALUE]"
  }
  </script>
  ```
  
  



## Other Resources

- [Dublic Core Meta Tags](http://www.seoconsultants.com/meta-tags/dublin/)
- [Apple Meta Tags](http://developer.apple.com/safari/library/documentation/appleapplications/reference/safarihtmlref/articles/metatags.html)
- [OpenGraph Meta Tags](http://opengraphprotocol.org/)
- [Link Tag Meaning](http://intertwingly.net/wiki/pie/LinkTagMeaning)
- [Google Chrome HTML5 Tags](http://www.html5rocks.com/)
