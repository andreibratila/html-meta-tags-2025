
from: https://gist.github.com/lancejpollard/1978404
from: https://github.com/kevinSuttle/html-meta-tags 

## Basic HTML Meta Tags

``` html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="150 words"/>
<meta name=generator content="Frontweaver 8.2">
<meta name="author" content="name name name">
<meta name="referrer" content="strict-origin-when-cross-origin">
<!-- 
  Available policies:
  - no-referrer: Never send referrer info
  - no-referrer-when-downgrade: Default (send full URL only on HTTPS→HTTPS)
  - strict-origin: Send domain only (no path/parameters)
  - strict-origin-when-cross-origin: ★ Recommended (full URL for same-origin, domain-only for cross-origin)
  - unsafe-url: Always send full URL (security risk)
-->
<meta name="robots" content="index,follow" />
<!-- 
  Available directives:
  - index/noindex: Allow/prevent page indexing
  - follow/nofollow: Allow/prevent link crawling
  - noimageindex: Prevent image indexing
  - none: Shorthand for noindex,nofollow
-->
<!-- only WebApp or pwa-->
<meta name="application-name" content="my app">
<!-- 
  Content Security Policy (CSP) Configuration
  Restricts which resources can be loaded to prevent XSS, data injection, and other attacks.
  
  Available Directives:
  Directive          | Description                               | Example
  -------------------|-------------------------------------------|-----------------------------
  default-src        | Fallback for unspecified resources         | default-src 'self'
  script-src         | Controls JavaScript sources               | script-src 'self' https://apis.google.com
  style-src          | Controls CSS sources                      | style-src 'self' 'unsafe-inline'
  img-src            | Controls image sources                    | img-src 'self' data: https://*.cdn.com
  font-src           | Controls font sources                     | font-src 'self' https://fonts.gstatic.com
  connect-src        | Controls fetch/XHR connections            | connect-src 'self' https://api.example.com
  frame-src          | Controls iframe sources                   | frame-src https://youtube.com
  media-src          | Controls audio/video sources              | media-src 'self' blob:
  object-src         | Controls plugin sources (Flash, etc.)     | object-src 'none' (recommended)
  base-uri           | Restricts URLs in <base> tags             | base-uri 'self'
  form-action        | Restricts form submission targets         | form-action 'self'

  Available Values:
  Value              | Usage
  -------------------|-------------------------------------------
  'self'            | Only allow from same origin
  'none'            | Block all resources
  'unsafe-inline'   | Allow inline JS/CSS (security risk)
  'unsafe-eval'     | Allow eval() (security risk)
  data:             | Allow data: URIs
  https:            | Only allow HTTPS resources
  Domains           | Specific allowed domains (https://example.com)

for only self-origin:
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

-->

<meta http-equiv="Content-Security-Policy" content="
  default-src 'self';
  script-src 'self' https://trusted.cdn.com 'unsafe-inline';
  style-src 'self' 'unsafe-inline';
  img-src 'self' data: https://*.imgur.com;
  font-src 'self' https://fonts.gstatic.com;
  frame-src 'none';
  object-src 'none';
  form-action 'self';
">


<meta name="theme-color" content="#3c790a" media="(prefers-color-scheme: light)">
<meta name="theme-color" content="#1a3e14" media="(prefers-color-scheme: dark)">
<meta name="color-scheme" content="light dark">
```

## OpenGraph Meta Tags

``` html
<meta property="og:title" content="The Rock"/>

<!-- Avalible: "website", "article", "product"
or custom types : https://ogp.me/#types
-->
<meta property="og:type" content="website" />

<meta property="og:url" content="https://www.imdb.com/title/tt0117500/"/>
<meta property="og:site_name" content="IMDb"/>
<meta property="og:description" content="A group of U.S. Marines, under command of..."/>
<meta property="og:locale" content="es_ES" />
<meta property="og:locale:alternate" content="fr_FR" />

<!-- Avalible: "a", "an", "the", "", "auto" -->
<meta property="og:determiner" content="the"> 


<meta property="og:image" content="https://example.com/ogp.jpg" />
<meta property="og:image:secure_url" content="https://secure.example.com/ogp.jpg" />
<meta property="og:image:type" content="image/jpeg" />
<meta property="og:image:width" content="400" />
<meta property="og:image:height" content="300" />
<meta property="og:image:alt" content="A shiny red apple with a bite taken out" />

<meta property="og:video" content="https://example.com/movie.swf" />
<meta property="og:video:secure_url" content="https://secure.example.com/movie.swf" />
<meta property="og:video:type" content="application/x-shockwave-flash" />
<meta property="og:video:width" content="400" />
<meta property="og:video:height" content="300" />

<meta property="og:audio" content="https://example.com/sound.mp3" />
<meta property="og:audio:secure_url" content="https://secure.example.com/sound.mp3" />
<meta property="og:audio:type" content="audio/mpeg" />


<meta name="fb:app_id" content="43929265776" />

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

#### Apple Meta Tags

``` html
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">

<!-- PWA or WebApp Apple -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-title" content="Mi App">
<!-- options: "default", "black", "black-translucent" --->
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">


<!-- Icons (minimum) -->
<link rel="apple-touch-icon" href="/apple-touch-icon-180x180.png" sizes="180x180">
<link rel="apple-touch-icon" href="/apple-touch-icon-167x167.png" sizes="167x167">
<link rel="apple-touch-icon" href="/apple-touch-icon-152x152.png" sizes="152x152">

<meta name="format-detection" content="telephone=no, email=no, date=no, address=no">

```


#### X / Twitter Meta Tags

``` html
<!-- REQUIRED CARD TYPE -->
<meta name="twitter:card" content="summary_large_image">
<!-- 
  Available card types:
  - summary: Standard card with thumbnail (300x300)
  - summary_large_image: Large image card (600x314)
  - player: Video/audio player card
  - app: Deep link to mobile app
-->

<!-- SITE/CREDENTIALS -->
<meta name="twitter:site" content="@company"> <!-- OR -->
<meta name="twitter:site:id" content="123456789"> <!-- Twitter Business ID -->
<meta name="twitter:creator" content="@author"> <!-- OR -->
<meta name="twitter:creator:id" content="987654321"> <!-- Author Twitter ID -->

<!-- CONTENT METADATA -->
<meta name="twitter:title" content="Page Title (70 chars max)">
<meta name="twitter:description" content="Description (200 chars max)">
<meta name="twitter:image" content="https://example.com/image.jpg"> <!-- 5MB max, 1200x630px optimal -->
<meta name="twitter:image:alt" content="Alt text for visually impaired (420 chars max)">

<!-- PLAYER CARD (Video/Audio) -->
<meta name="twitter:player" content="https://example.com/player">
<meta name="twitter:player:width" content="1280">
<meta name="twitter:player:height" content="720">
<meta name="twitter:player:stream" content="https://example.com/video.mp4">

<!-- APP CARD (Mobile Deep Linking) -->
<!-- iOS -->
<meta name="twitter:app:name:iphone" content="App Name">
<meta name="twitter:app:id:iphone" content="ios_app_store_id">
<meta name="twitter:app:url:iphone" content="appname://">
<meta name="twitter:app:name:ipad" content="App Name (iPad)">
<meta name="twitter:app:id:ipad" content="ios_app_store_id">
<meta name="twitter:app:url:ipad" content="appname://">

<!-- Android -->
<meta name="twitter:app:name:googleplay" content="App Name">
<meta name="twitter:app:id:googleplay" content="com.company.app">
<meta name="twitter:app:url:googleplay" content="appname://">

<!-- FALLBACK NOTES:
- If Twitter tags are missing, X falls back to OpenGraph equivalents
- Required minimum for rich cards: 
  twitter:card + twitter:title + twitter:description + twitter:image
-->
```

#### Rails Meta Tags

``` html
<meta name="csrf-param" content="authenticity_token"/>
<meta name="csrf-token" content="/bZVwvomkAnwAI1Qd37lFeewvpOIiackk9121fFwWwc="/>
```

## HTML Link Tags

``` html
<!-- Favicon -->
<link rel="icon" href="/favicon.ico" type="image/x-icon">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">

<!-- Canonical URL (para SEO) -->
<link rel="canonical" href="https://yourdomain.com/about">

<!-- RSS/Atom (for blogs) -->
<link rel="alternate" type="application/rss+xml" title="RSS" href="/feed.xml">

<!-- Preconexión (performance improvement) -->
<link rel="preconnect" href="https://cdn.tudominio.com">

<!-- OpenSearch (custom search) -->
<link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="Search in my Site e">

<!-- Verificación redes sociales (IndieWeb) -->
<link rel="me" href="https://github.com/yourUser">
<link rel="me" href="https://twitter.com/yourUser">

<!-- PWA -->
<link rel="manifest" href="/manifest.webmanifest">

<link rel="alternate" type="application/rss+xml" title="RSS" href="http://feeds.feedburner.com/martini" />

<link rel='shortlink' href='http://blog.unto.net/?p=353' />
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

- [Apple Meta Tags](http://developer.apple.com/safari/library/documentation/appleapplications/reference/safarihtmlref/articles/metatags.html)
- [OpenGraph Meta Tags](http://opengraphprotocol.org/)
- [FaceBook Meta Tags](http://developers.facebook.com/docs/sharing/webmasters/)
- [Twitter/x Meta Tags](https://developer.x.com/en/docs/x-for-websites/cards/overview/markup)
- [HTML5 Meta Tags](https://html.spec.whatwg.org/multipage/semantics.html#the-meta-element)
- [Google Chrome HTML5 Tags](http://www.html5rocks.com/)
