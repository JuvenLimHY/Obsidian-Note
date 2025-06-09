# nmap 

```
# Nmap 7.95 scan initiated Mon Jun  9 10:31:12 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/tcp80/tcp_80_http_nmap.txt -oX /home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/tcp80/xml/tcp_80_http_nmap.xml 192.168.114.111
Warning: Hit PCRE_ERROR_MATCHLIMIT when probing for service http with the regex '^HTTP/1\.1 \d\d\d (?:[^\r\n]*\r\n(?!\r\n))*?.*\r\nServer: Virata-EmWeb/R([\d_]+)\r\nContent-Type: text/html; ?charset=UTF-8\r\nExpires: .*<title>HP (Color |)LaserJet ([\w._ -]+)&nbsp;&nbsp;&nbsp;'
Nmap scan report for 192.168.114.111
Host is up, received user-set (0.24s latency).
Scanned at 2025-06-09 10:31:12 EDT for 670s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON          VERSION
80/tcp open  http    syn-ack ttl 127 Microsoft IIS httpd 10.0
|_http-title: Home
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-feed: Couldn't find any feeds.
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=192.168.114.111
|     
|     Path: http://192.168.114.111:80/nicepage.js
|     Line number: 36
|     Comment: 
|         /*!
|          * gumshoejs v5.1.2
|          * A simple, framework-agnostic scrollspy script.
|          * (c) 2019 Chris Ferdinandi
|          * MIT License
|          * http://github.com/cferdinandi/gumshoe
|          */
|     
|     Path: http://192.168.114.111:80/nicepage.js
|     Line number: 7
|     Comment: 
|         /*! ieee754. BSD-3-Clause License. Feross Aboukhadijeh <https://feross.org/opensource> */
|     
|     Path: http://192.168.114.111:80/r.href1v.crossDomain1Wt.protocol1%22/%221Wt.host11r.protocol1%22/%221r.host%7Dcatch1e1%7Bv.crossDomain110%7D%7Dif1v.data11v.processData11%22string%2211typeof
|     Line number: 7
|     Comment: 
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         -->
|     
|     Path: http://192.168.114.111:80/nicepage.js
|     Line number: 22
|     Comment: 
|         /*!
|         Waypoints - 4.0.1
|         Copyright \xC2\xA9 2011-2016 Caleb Troughton
|         Licensed under the MIT license.
|         https://github.com/imakewebthings/waypoints/blob/master/licenses.txt
|         */
|     
|     Path: http://192.168.114.111:80/jquery.js
|     Line number: 1
|     Comment: 
|         /*! jQuery v3.5.1 | (c) JS Foundation and other contributors | jquery.org/license */
|     
|     Path: http://192.168.114.111:80/nicepage.js
|     Line number: 11
|     Comment: 
|         /*! PhotoSwipe Default UI - 4.1.3 - 2019-01-08
|         * http://photoswipe.com
|         * Copyright (c) 2019 Dmitry Semenov; */
|     
|     Path: http://192.168.114.111:80/nicepage.js
|     Line number: 8
|     Comment: 
|         /*! PhotoSwipe - v4.1.3 - 2019-01-08
|         * http://photoswipe.com
|         * Copyright (c) 2019 Dmitry Semenov; */
|     
|     Path: http://192.168.114.111:80/nicepage.js
|     Line number: 2
|     Comment: 
|         /*!
|          * https://github.com/gilmoreorless/css-background-parser
|          * Copyright \xC2\xA9 2015 Gilmore Davidson under the MIT license: http://gilmoreorless.mit-license.org/
|          */
|     
|     Path: http://192.168.114.111:80/nicepage.js
|     Line number: 29
|     Comment: 
|         /*!
|          * JavaScript Cookie v2.2.1
|          * https://github.com/js-cookie/js-cookie
|          *
|          * Copyright 2006, 2015 Klaus Hartl & Fagner Brack
|          * Released under the MIT license
|          */
|     
|     Path: http://192.168.114.111:80/nicepage.js
|     Line number: 14
|     Comment: 
|         /*!
|          * skrollr core
|          *
|          * Alexander Prinzhorn - https://github.com/Prinzhorn/skrollr
|          *
|          * Free to use under terms of MIT license
|_         */
|_http-generator: Nicepage 4.16.0, nicepage.com
| http-headers: 
|   Content-Length: 44165
|   Content-Type: text/html
|   Last-Modified: Wed, 31 Aug 2022 23:27:43 GMT
|   Accept-Ranges: bytes
|   ETag: "b3c8d44491bdd81:0"
|   Server: Microsoft-IIS/10.0
|   Date: Mon, 09 Jun 2025 14:31:22 GMT
|   Connection: close
|   
|_  (Request type: HEAD)
|_http-malware-host: Host appears to be clean
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-vhosts: 
|_128 names had status 200
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Allowed User Agents: 
|     Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)
|     libwww
|     lwp-trivial
|     libcurl-agent/1.0
|     PHP/
|     Python-urllib/2.5
|     GT::WWW
|     Snoopy
|     MFC_Tear_Sample
|     HTTP::Lite
|     PHPCrawl
|     URI::Fetch
|     Zend_Http_Client
|     http client
|     PECL::HTTP
|     Wget/1.13.4 (linux-gnu)
|_    WWW-Mechanize/1.34
| http-fileupload-exploiter: 
|   
|     Couldn't find a file-type field.
|   
|_    Couldn't find a file-type field.
|_http-backup-finder: ERROR: Script execution failed (use -d to debug)
|_http-exif-spider: ERROR: Script execution failed (use -d to debug)
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-date: Mon, 09 Jun 2025 14:31:23 GMT; -1s from local time.
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-server-header: Microsoft-IIS/10.0
| http-dombased-xss: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=192.168.114.111
|   Found the following indications of potential DOM based XSS: 
|     
|     Source: window.open(i.href,"pswp_share","scrollbars=yes,resizable=yes,toolbar=no,"+"location=yes,width=550,height=420,top=100,left="+(window.screen?Math.round(screen.width/2-275)
|_    Pages: http://192.168.114.111:80/nicepage.js
| http-php-version: Logo query returned unknown hash eded47b333bb1de63c25d3d7a64a1581
|_Credits query returned unknown hash eded47b333bb1de63c25d3d7a64a1581
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-errors: Couldn't find any error pages.
|_http-chrono: Request times for /; avg: 1090.59ms; min: 1047.64ms; max: 1136.16ms
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1; css: 2; html: 3; js: 2
|     /images/
|       jpg: 5; png: 4
|   Longest directory structure:
|     Depth: 1
|     Dir: /images/
|   Total files found (by extension):
|_    Other: 1; css: 2; html: 3; jpg: 5; js: 2; png: 4
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=192.168.114.111
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://192.168.114.111:80/
|     Form id: email-f2a8
|     Form action: //publish.nicepage.com/Form/Process
|     
|     Path: http://192.168.114.111:80/Home.html
|     Form id: email-f2a8
|_    Form action: //publish.nicepage.com/Form/Process
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
|_http-mobileversion-checker: No mobile version detected.
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
| http-enum: 
|_  /home.html: Possible admin folder
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 10:42:22 2025 -- 1 IP address (1 host up) scanned in 670.38 seconds

```

# nikto 

```

- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          192.168.114.111
+ Target Hostname:    192.168.114.111
+ Target Port:        80
+ Start Time:         2025-06-09 10:31:15 (GMT-4)
---------------------------------------------------------------------------
+ Server: Microsoft-IIS/10.0
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ OPTIONS: Allowed HTTP Methods: OPTIONS, TRACE, GET, HEAD, POST .
+ OPTIONS: Public HTTP Methods: OPTIONS, TRACE, GET, HEAD, POST .
+ 7734 requests: 4 error(s) and 4 item(s) reported on remote host
+ End Time:           2025-06-09 11:06:28 (GMT-4) (2113 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested

```

# screenshot


# whatweb

```
WhatWeb report for http://192.168.114.111:80
Status    : 200 OK
Title     : Home
IP        : 192.168.114.111
Country   : RESERVED, ZZ

Summary   : HTML5, HTTPServer[Microsoft-IIS/10.0], JQuery, MetaGenerator[Nicepage 4.16.0, nicepage.com], Microsoft-IIS[10.0], Open-Graph-Protocol[website], Script[application/ld+json,text/javascript]

Detected Plugins:
[ HTML5 ]
	HTML version 5, detected by the doctype declaration


[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	String       : Microsoft-IIS/10.0 (from server string)

[ JQuery ]
	A fast, concise, JavaScript that simplifies how to traverse
	HTML documents, handle events, perform animations, and add
	AJAX.

	Website     : http://jquery.com/

[ MetaGenerator ]
	This plugin identifies meta generator tags and extracts its
	value.

	String       : Nicepage 4.16.0, nicepage.com

[ Microsoft-IIS ]
	Microsoft Internet Information Services (IIS) for Windows
	Server is a flexible, secure and easy-to-manage Web server
	for hosting anything on the Web. From media streaming to
	web application hosting, IIS's scalable and open
	architecture is ready to handle the most demanding tasks.

	Version      : 10.0
	Website     : http://www.iis.net/

[ Open-Graph-Protocol ]
	The Open Graph protocol enables you to integrate your Web
	pages into the social graph. It is currently designed for
	Web pages representing profiles of real-world things .
	things like movies, sports teams, celebrities, and
	restaurants. Including Open Graph tags on your Web page,
	makes your page equivalent to a Facebook Page.

	Version      : website

[ Script ]
	This plugin detects instances of script HTML elements and
	returns the script language/type.

	String       : application/ld+json,text/javascript

HTTP Headers:
	HTTP/1.1 200 OK
	Content-Type: text/html
	Content-Encoding: gzip
	Last-Modified: Wed, 31 Aug 2022 23:27:43 GMT
	Accept-Ranges: bytes
	ETag: "80c1d24491bdd81:0"
	Vary: Accept-Encoding
	Server: Microsoft-IIS/10.0
	Date: Mon, 09 Jun 2025 14:31:14 GMT
	Connection: close
	Content-Length: 11182



```

# scrapy

```

```
# dirbuster
## dirsearch

### directory 

```
Configuration {
    kind: "configuration",
    wordlist: "/root/.local/share/AutoRecon/wordlists/dirbuster.txt",
    config: "/etc/feroxbuster/ferox-config.toml",
    proxy: "",
    replay_proxy: "",
    server_certs: [],
    client_cert: "",
    client_key: "",
    target_url: "http://192.168.114.111:80/",
    status_codes: [
        100,
        101,
        102,
        200,
        201,
        202,
        203,
        204,
        205,
        206,
        207,
        208,
        226,
        300,
        301,
        302,
        303,
        304,
        305,
        307,
        308,
        400,
        401,
        402,
        403,
        404,
        405,
        406,
        407,
        408,
        409,
        410,
        411,
        412,
        413,
        414,
        415,
        416,
        417,
        418,
        421,
        422,
        423,
        424,
        426,
        428,
        429,
        431,
        451,
        500,
        501,
        502,
        503,
        504,
        505,
        506,
        507,
        508,
        510,
        511,
        103,
        425,
    ],
    replay_codes: [
        100,
        101,
        102,
        200,
        201,
        202,
        203,
        204,
        205,
        206,
        207,
        208,
        226,
        300,
        301,
        302,
        303,
        304,
        305,
        307,
        308,
        400,
        401,
        402,
        403,
        404,
        405,
        406,
        407,
        408,
        409,
        410,
        411,
        412,
        413,
        414,
        415,
        416,
        417,
        418,
        421,
        422,
        423,
        424,
        426,
        428,
        429,
        431,
        451,
        500,
        501,
        502,
        503,
        504,
        505,
        506,
        507,
        508,
        510,
        511,
        103,
        425,
    ],
    filter_status: [],
    client: Client {
        accepts: Accepts,
        proxies: [
            Proxy(
                System(
                    {},
                ),
                None,
            ),
        ],
        referer: true,
        default_headers: {
            "accept": "*/*",
            "user-agent": "feroxbuster/2.11.0",
        },
        timeout: 7s,
    },
    replay_client: None,
    threads: 10,
    timeout: 7,
    verbosity: 1,
    silent: false,
    quiet: true,
    output_level: Quiet,
    auto_bail: false,
    auto_tune: false,
    requester_policy: Default,
    json: false,
    output: "/home/kali/OSCP/Exam/AD/192.168.114.111/results/192.168.114.111/scans/tcp80/tcp_80_http_feroxbuster_dirbuster.txt",
    debug_log: "",
    user_agent: "feroxbuster/2.11.0",
    random_agent: false,
    redirects: true,
    insecure: true,
    extensions: [
        "txt",
        "html",
        "php",
        "asp",
        "aspx",
        "jsp",
    ],
    methods: [
        "GET",
    ],
    data: [],
    headers: {},
    queries: [],
    no_recursion: true,
    extract_links: true,
    add_slash: false,
    stdin: false,
    depth: 4,
    scan_limit: 0,
    parallel: 0,
    rate_limit: 0,
    filter_size: [],
    filter_line_count: [],
    filter_word_count: [],
    filter_regex: [],
    dont_filter: false,
    resumed: false,
    resume_from: "",
    save_state: true,
    time_limit: "",
    filter_similar: [],
    url_denylist: [],
    regex_denylist: [],
    collect_extensions: false,
    dont_collect: [
        "tif",
        "tiff",
        "ico",
        "cur",
        "bmp",
        "webp",
        "svg",
        "png",
        "jpg",
        "jpeg",
        "jfif",
        "gif",
        "avif",
        "apng",
        "pjpeg",
        "pjp",
        "mov",
        "wav",
        "mpg",
        "mpeg",
        "mp3",
        "mp4",
        "m4a",
        "m4p",
        "m4v",
        "ogg",
        "webm",
        "ogv",
        "oga",
        "flac",
        "aac",
        "3gp",
        "css",
        "zip",
        "xls",
        "xml",
        "gz",
        "tgz",
    ],
    collect_backups: false,
    backup_extensions: [
        "~",
        ".bak",
        ".bak2",
        ".old",
        ".1",
    ],
    collect_words: false,
    force_recursion: false,
    update_app: false,
    scan_dir_listings: false,
    request_file: "",
    protocol: "https",
    limit_bars: 0,
}
200      GET       14l       88w     5675c http://192.168.114.111/images/1633659-c312dd2d.png
200      GET       70l      284w     4720c http://192.168.114.111/Contact.html
200      GET       13l       54w     3857c http://192.168.114.111/images/4457024-0e170e4c.png
200      GET       70l      284w     4714c http://192.168.114.111/About.html
200      GET       15l       53w     3497c http://192.168.114.111/images/840781-6ced8a49.png
200      GET      365l     2965w    44110c http://192.168.114.111/Home.html
200      GET       11l       58w     2670c http://192.168.114.111/images/6646730-387c719a.png
200      GET        2l     1297w    89476c http://192.168.114.111/jquery.js
200      GET      128l      739w   124162c http://192.168.114.111/images/kj.jpg
200      GET      155l      709w   104088c http://192.168.114.111/images/ggg.jpg
200      GET      165l     1084w   124901c http://192.168.114.111/images/bn.jpg
200      GET      139l      770w    70330c http://192.168.114.111/images/nn.jpg
200      GET      121l      801w   139255c http://192.168.114.111/images/5178414.jpg
200      GET       42l     4104w   243109c http://192.168.114.111/nicepage.js
200      GET     1862l     3406w    30611c http://192.168.114.111/Home.css
200      GET    37951l    82833w  1284685c http://192.168.114.111/nicepage.css
200      GET      365l     2967w    44165c http://192.168.114.111/
200      GET        0l        0w        0c http://192.168.114.111/About.css
200      GET        0l        0w        0c http://192.168.114.111/Contact.css
403      GET       29l       92w     1233c http://192.168.114.111/Images/
200      GET      365l     2967w    44165c http://192.168.114.111/Index.html
200      GET       70l      284w     4714c http://192.168.114.111/about.html
200      GET       70l      284w     4720c http://192.168.114.111/contact.html
200      GET      365l     2965w    44110c http://192.168.114.111/home.html
403      GET       29l       92w     1233c http://192.168.114.111/images/
200      GET      365l     2967w    44165c http://192.168.114.111/index.html
403      GET       29l       92w     1233c http://192.168.114.111/IMAGES/
200      GET      365l     2965w    44110c http://192.168.114.111/HOME.html
200      GET       70l      284w     4714c http://192.168.114.111/ABOUT.html
200      GET       70l      284w     4720c http://192.168.114.111/CONTACT.html

```
### files

```

```
# curl 

```
HTTP/1.1 200 OK
Content-Type: text/html
Last-Modified: Wed, 31 Aug 2022 23:27:43 GMT
Accept-Ranges: bytes
ETag: "b3c8d44491bdd81:0"
Server: Microsoft-IIS/10.0
Date: Mon, 09 Jun 2025 14:31:14 GMT
Content-Length: 44165

<!DOCTYPE html>
<html style="font-size: 16px;" lang="en"><head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta charset="utf-8">
    <meta name="keywords" content="​Library Education, ​Meet our Principal, ​Helping each child find and follow their best learning path.">
    <meta name="description" content="">
    <title>Home</title>
    <link rel="stylesheet" href="nicepage.css" media="screen">
<link rel="stylesheet" href="Home.css" media="screen">
    <script class="u-script" type="text/javascript" src="jquery.js" "="" defer=""></script>
    <script class="u-script" type="text/javascript" src="nicepage.js" "="" defer=""></script>
    <meta name="generator" content="Nicepage 4.16.0, nicepage.com">
    <link id="u-theme-google-font" rel="stylesheet" href="https://fonts.googleapis.com/css?family=Raleway:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i|Open+Sans:300,300i,400,400i,500,500i,600,600i,700,700i,800,800i">
    <link id="u-page-google-font" rel="stylesheet" href="https://fonts.googleapis.com/css?family=Raleway:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i">









    <script type="application/ld+json">{
		"@context": "http://schema.org",
		"@type": "Organization",
		"name": ""
}</script>
    <meta name="theme-color" content="#2799b1">
    <meta property="og:title" content="Home">
    <meta property="og:type" content="website">
  </head>
  <body data-home-page="Home.html" data-home-page-title="Home" class="u-body u-xl-mode" data-lang="en"><header class="u-clearfix u-header u-header" id="sec-9c34"><div class="u-clearfix u-sheet u-sheet-1">
        <nav class="u-menu u-menu-dropdown u-offcanvas u-menu-1" data-responsive-from="XL">
          <div class="menu-collapse" style="font-size: 1rem; letter-spacing: 0px; font-weight: 500;">
            <a class="u-button-style u-custom-active-color u-custom-border u-custom-border-color u-custom-hover-color u-custom-left-right-menu-spacing u-custom-padding-bottom u-custom-text-active-color u-custom-text-color u-custom-text-hover-color u-custom-top-bottom-menu-spacing u-nav-link u-text-active-palette-1-base u-text-hover-palette-2-base" href="#">
              <svg class="u-svg-link" viewBox="0 0 24 24"><use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#menu-hamburger"></use></svg>
              <svg class="u-svg-content" version="1.1" id="menu-hamburger" viewBox="0 0 16 16" x="0px" y="0px" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg"><g><rect y="1" width="16" height="2"></rect><rect y="7" width="16" height="2"></rect><rect y="13" width="16" height="2"></rect>
</g></svg>
            </a>
          </div>
          <div class="u-nav-container">
            <ul class="u-nav u-spacing-2 u-unstyled u-nav-1"><li class="u-nav-item"><a class="u-active-grey-5 u-button-style u-hover-grey-10 u-nav-link u-text-active-grey-90 u-text-grey-90 u-text-hover-grey-90" href="Home.html" style="padding: 10px 20px;">Home</a>
</li><li class="u-nav-item"><a class="u-active-grey-5 u-button-style u-hover-grey-10 u-nav-link u-text-active-grey-90 u-text-grey-90 u-text-hover-grey-90" href="About.html" style="padding: 10px 20px;">About</a>
</li><li class="u-nav-item"><a class="u-active-grey-5 u-button-style u-hover-grey-10 u-nav-link u-text-active-grey-90 u-text-grey-90 u-text-hover-grey-90" href="Contact.html" style="padding: 10px 20px;">Contact</a>
</li></ul>
          </div>
          <div class="u-nav-container-collapse">
            <div class="u-black u-container-style u-inner-container-layout u-opacity u-opacity-95 u-sidenav">
              <div class="u-inner-container-layout u-sidenav-overflow">
                <div class="u-menu-close"></div>
                <ul class="u-align-center u-nav u-popupmenu-items u-unstyled u-nav-2"><li class="u-nav-item"><a class="u-button-style u-nav-link" href="Home.html" style="padding: 10px 20px;">Home</a>
</li><li class="u-nav-item"><a class="u-button-style u-nav-link" href="About.html" style="padding: 10px 20px;">About</a>
</li><li class="u-nav-item"><a class="u-button-style u-nav-link" href="Contact.html" style="padding: 10px 20px;">Contact</a>
</li></ul>
              </div>
            </div>
            <div class="u-black u-menu-overlay u-opacity u-opacity-70"></div>
          </div>
        </nav>
      </div></header>
    <section class="u-align-center u-clearfix u-image u-valign-middle-md u-valign-middle-sm u-valign-middle-xs u-section-1" id="sec-6c81" data-image-width="1980" data-image-height="1114">
      <div class="u-clearfix u-gutter-0 u-layout-wrap u-layout-wrap-1">
        <div class="u-layout" style="">
          <div class="u-layout-row" style="">
            <div class="u-align-left u-container-style u-layout-cell u-left-cell u-shape-rectangle u-size-20-lg u-size-20-xl u-size-23-md u-size-23-sm u-size-23-xs u-size-xs-60 u-layout-cell-1" src="">
              <div class="u-container-layout u-valign-middle u-container-layout-1">
                <h1 class="u-text u-text-body-alt-color u-text-1" data-animation-name="fadeIn" data-animation-duration="1000" data-animation-direction="Left" data-animation-delay="250"> Library Education</h1>
                <p class="u-text u-text-body-alt-color u-text-2" data-animation-name="fadeIn" data-animation-duration="1000" data-animation-direction="Up" data-animation-delay="250">Enjoy ​access to high quality information resources and services through a team of skilled and knowledgeable staff and welcoming physical environments.</p>
                <a href="https://nicepage.best" class="u-border-none u-btn u-btn-round u-button-style u-palette-3-base u-radius-10 u-text-palette-1-base u-btn-1" data-animation-name="fadeIn" data-animation-duration="1000" data-animation-direction="Up" data-animation-delay="500">learn more</a>
                <p class="u-text u-text-body-alt-color u-text-3" data-animation-name="fadeIn" data-animation-duration="1000" data-animation-direction="Up" data-animation-delay="500">Images from <a href="https://www.freepik.com/psd/abstract-background" class="u-active-none u-border-2 u-border-active-palette-3-base u-border-hover-palette-3-base u-border-white u-btn u-button-link u-button-style u-hover-none u-none u-text-body-alt-color u-btn-2">Freepik</a>
                </p>
              </div>
            </div>
            <div class="u-align-center u-container-style u-image u-layout-cell u-right-cell u-size-37-md u-size-37-sm u-size-37-xs u-size-40-lg u-size-40-xl u-size-xs-60 u-image-1" data-image-width="1422" data-image-height="900">
              <div class="u-container-layout u-container-layout-2" src=""></div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="u-align-center u-clearfix u-valign-middle u-white u-section-2" id="carousel_2f1f">
      <div class="u-expanded-width u-gradient u-opacity u-opacity-55 u-shape u-shape-rectangle u-shape-1" data-animation-name="rollIn" data-animation-duration="1000" data-animation-direction=""></div>
      <div class="u-clearfix u-gutter-40 u-layout-spacing-vertical u-layout-wrap u-layout-wrap-1">
        <div class="u-gutter-0 u-layout">
          <div class="u-layout-row">
            <div class="u-size-31 u-size-60-md">
              <div class="u-layout-col">
                <div class="u-container-style u-hidden-md u-hidden-sm u-hidden-xs u-layout-cell u-right-cell u-size-20 u-layout-cell-1" wfd-invisible="true">
                  <div class="u-container-layout u-container-layout-1"></div>
                </div>
                <div class="u-align-center u-container-style u-layout-cell u-radius-20 u-right-cell u-shape-round u-size-40 u-white u-layout-cell-2" data-animation-name="fadeIn" data-animation-duration="1000" data-animation-direction="Left" data-animation-delay="250">
                  <div class="u-container-layout u-valign-top u-container-layout-2">
                    <img class="u-expanded-width u-image u-image-round u-radius-20 u-image-1" src="images/bn.jpg" alt="" data-image-width="800" data-image-height="800" data-animation-name="fadeIn" data-animation-duration="2000" data-animation-direction="Left" data-animation-delay="250">
                    <h5 class="u-text u-text-1"> Experience what you have learned</h5>
                    <p class="u-text u-text-2"> We treat each child as a unique individual and aim to instil in them a sense of curiosity and a love of learning that will continue throughout their lives.</p>
                    <a href="https://nicepage.com" class="u-border-none u-btn u-btn-round u-button-style u-palette-3-base u-radius-10 u-text-palette-1-base u-btn-1" data-animation-name="rollIn" data-animation-duration="1000" data-animation-direction="" data-animation-delay="500">learn more</a>
                  </div>
                </div>
              </div>
            </div>
            <div class="u-size-29 u-size-60-md">
              <div class="u-layout-col">
                <div class="u-align-center u-container-style u-layout-cell u-left-cell u-radius-20 u-size-40 u-layout-cell-3" data-animation-name="zoomIn" data-animation-duration="2000" data-animation-direction="">
                  <div class="u-container-layout u-valign-middle-md u-valign-middle-sm u-valign-middle-xs u-valign-top-lg u-valign-top-xl u-container-layout-3" src="">
                    <img class="u-image u-image-round u-radius-20 u-image-2" src="images/kj.jpg" data-image-width="1200" data-image-height="1002" data-animation-name="fadeIn" data-animation-duration="1000" data-animation-direction="Right" data-animation-delay="250">
                  </div>
                </div>
                <div class="u-align-center u-container-style u-layout-cell u-left-cell u-size-20 u-white u-layout-cell-4">
                  <div class="u-container-layout u-valign-top u-container-layout-4">
                    <h3 class="u-text u-text-default u-text-3">Our Collection</h3>
                    <p class="u-text u-text-4"> Our library boasts over 2.7 million items and supports students in teaching and research.&nbsp;<br>We subscribe to an increasing number of electronic journals and electronic books that are available to students and staff online at any time.<br>
                    </p>
                    <p class="u-text u-text-default u-text-5">Images from <a href="https://www.freepik.com/psd/woman" class="u-border-1 u-border-active-palette-1-base u-border-black u-border-hover-palette-1-base u-btn u-button-link u-button-style u-none u-text-body-color u-btn-2">Freepik</a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="u-align-center u-clearfix u-palette-3-base u-section-3" id="carousel_aed0">
      <div class="u-gradient u-opacity u-opacity-55 u-shape u-shape-rectangle u-shape-1" data-animation-name="fadeIn" data-animation-duration="1000" data-animation-direction="Left"></div>
      <div class="u-list u-list-1">
        <div class="u-repeater u-repeater-1">
          <div class="u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-white u-list-item-1" data-animation-name="flipIn" data-animation-duration="1000" data-animation-direction="X" data-animation-delay="250">
            <div class="u-container-layout u-similar-container u-valign-top u-container-layout-1">
              <h3 class="u-text u-text-default u-text-palette-1-base u-text-1"> Digitisation</h3>
              <p class="u-text u-text-2"> Digitisation is a wonderful way of increasing access to unique collections that are not readily accessible and visible. Our Digitisation Unit offers an on-demand digitisation service that includes the digitisation and digital preservation of paper documents, photographs, maps, slides and negatives and 3D objects to enable access to and preservation of these collections.</p>
            </div>
          </div>
          <div class="u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-white" data-animation-name="flipIn" data-animation-duration="1000" data-animation-direction="X" data-animation-delay="250">
            <div class="u-container-layout u-similar-container u-valign-top u-container-layout-2">
              <h3 class="u-text u-text-default u-text-palette-1-base u-text-3"> Bindery</h3>
              <p class="u-text u-text-4">We have a well-established bindery unit which offers high-standard and professional binding services to our members, students, academic departments as well as private clients. The service can be used for any private publications, assignments, articles, and dissertations.</p>
            </div>
          </div>
          <div class="u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-white" data-animation-name="flipIn" data-animation-duration="1000" data-animation-direction="X" data-animation-delay="250">
            <div class="u-container-layout u-similar-container u-valign-top u-container-layout-3">
              <h3 class="u-text u-text-default u-text-palette-1-base u-text-5"> Plagiarism</h3>
              <p class="u-text u-text-6"> Plagiarism is defined as the presentation of someone else’s work, words, images, ideas, opinions, discoveries, artwork, music, recordings or computer-generated work - whether published or not, as one’s own work without properly acknowledging the source.<br>
                <br>We offer training Sessions are offered by request or on Tuesdays and Thursdays
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="u-gradient u-shape u-shape-circle u-shape-2" data-animation-name="customAnimation" data-animation-duration="1000" data-animation-direction="" data-animation-delay="250"></div>
    </section>
    <section class="u-clearfix u-section-4" id="carousel_08cf">
      <div class="u-clearfix u-sheet u-valign-middle u-sheet-1">
        <div class="u-expanded-width-lg u-expanded-width-md u-expanded-width-sm u-expanded-width-xs u-gradient u-shape u-shape-rectangle u-shape-1"></div>
        <img class="u-align-left u-image u-image-round u-radius-20 u-image-1" data-image-width="900" data-image-height="900" src="images/5178414.jpg">
        <div class="u-container-style u-grey-5 u-group u-radius-20 u-shape-round u-group-1">
          <div class="u-container-layout u-valign-middle-lg u-valign-middle-md u-valign-middle-sm u-valign-middle-xl u-container-layout-1">
            <h3 class="u-align-left u-text u-text-default u-text-1">Interlending&nbsp;</h3>
            <p class="u-align-left u-text u-text-2"> The primary purpose of interlibrary loans (ILL) is to support research and teaching at the Library by obtaining documents not available in our library from other libraries and also to supply documents requested by other libraries. Documents are requested from local libraries as well as international libraries.&nbsp;<br>Interlending is a service that can be used to obtain books and articles that are not available at the home library, from national and international libraries. If the item you need to get hold of is not in our library catalogue, electronic journals A-Z list, Google or Google Scholar, you can request the item from another local or international library.
            </p>
            <p class="u-align-left u-text u-text-default u-text-3">Images from <a href="https://www.freepik.com/psd/woman" class="u-border-1 u-border-active-palette-1-base u-border-black u-border-hover-palette-1-base u-btn u-button-link u-button-style u-none u-text-body-color u-btn-1">Freepik</a>
            </p>
            <a href="https://nicepage.com/c/text-button-html-templates" class="u-border-none u-btn u-btn-round u-button-style u-palette-3-base u-radius-10 u-text-palette-1-base u-btn-2">learn more</a>
          </div>
        </div>
        <div class="u-gradient u-shape u-shape-circle u-shape-2"></div>
      </div>
    </section>
    <section class="u-align-center u-clearfix u-grey-5 u-section-5" id="sec-686e">
      <div class="u-clearfix u-sheet u-valign-middle u-sheet-1">
        <h2 class="u-text u-text-default u-text-1"> Get to know our principles</h2>
        <div class="u-list u-list-1">
          <div class="u-repeater u-repeater-1">
            <div class="u-align-left u-container-style u-custom-item u-gradient u-list-item u-radius-20 u-repeater-item u-shape-round u-list-item-1">
              <div class="u-container-layout u-similar-container u-container-layout-1">
                <h4 class="u-custom-item u-text u-text-body-alt-color u-text-default u-text-2"> Learning is an active process</h4>
                <p class="u-custom-item u-text u-text-body-alt-color u-text-default u-text-3"> The Library aims to proactively develop and deliver high-quality innovative library services. The Library makes available information resources and enabling spaces that support learning and research.</p>
              </div>
            </div>
            <div class="u-align-left u-container-style u-custom-item u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-white u-list-item-2">
              <div class="u-container-layout u-similar-container u-container-layout-2">
                <h4 class="u-custom-item u-text u-text-default u-text-4">Incorporating technology</h4>
                <p class="u-custom-item u-text u-text-default u-text-5"> The Library maximises the use of technology to support its core activities and allows the influence of the digital era to transcend academic boundaries and stimulate transdisciplinary study by offering access to new digital technologies and high-tech services.&nbsp;</p>
              </div>
            </div>
            <div class="u-align-left u-container-style u-custom-item u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-white u-list-item-3">
              <div class="u-container-layout u-similar-container u-container-layout-3">
                <h4 class="u-custom-item u-text u-text-default u-text-6">Collating from various sources</h4>
                <p class="u-custom-item u-text u-text-default u-text-7"> The Library provides access to a wide range of information resources, such as books, journals, reports, standards, and special collections.&nbsp;<br>
                  <br>We raise awareness and builds on our reputation by continually carrying out new initiatives, which are recognisable, fair, sustainable, responsive, and inventive.
                </p>
              </div>
            </div>
            <div class="u-align-left u-container-style u-custom-item u-gradient u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-list-item-4">
              <div class="u-container-layout u-similar-container u-container-layout-4">
                <h4 class="u-custom-item u-text u-text-body-alt-color u-text-default u-text-8">Sustainability</h4>
                <p class="u-custom-item u-text u-text-body-alt-color u-text-default u-text-9"> The expertise of our staff support and enable the academic activities of the University. All these efforts are grounded in the library's goals for teaching, learning, and research; including the research themes that are linked to the achievement of the United Nations' 2030 Agenda for Sustainable Development Goals, all of which are based on sustainability.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="u-clearfix u-grey-5 u-section-6" id="sec-bf70">
      <div class="u-clearfix u-sheet u-sheet-1">
        <div class="u-expanded-width-xs u-gradient u-shape u-shape-rectangle u-shape-1"></div>
        <img class="u-expanded-width-xs u-image u-image-1" src="images/nn.jpg" data-image-width="1080" data-image-height="1080">
        <div class="u-container-style u-group u-radius-20 u-shape-round u-white u-group-1">
          <div class="u-container-layout u-valign-middle u-container-layout-1">
            <h2 class="u-text u-text-1"> Helping each member find and follow their best learning path.</h2>
            <p class="u-text u-text-2">Image from <a href="https://www.freepik.com/photos/school" class="u-active-none u-border-1 u-border-active-palette-1-base u-border-grey-75 u-border-hover-palette-1-base u-btn u-button-link u-button-style u-hover-none u-none u-text-body-color u-btn-1" target="_blank">Freepik</a>
            </p>
            <a href="https://nicepage.com/html-website-builder" class="u-border-none u-btn u-btn-round u-button-style u-palette-3-base u-radius-10 u-text-palette-1-base u-btn-2">learn more</a>
          </div>
        </div>
        <div class="u-list u-list-1">
          <div class="u-repeater u-repeater-1">
            <div class="u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-white u-list-item-1">
              <div class="u-container-layout u-similar-container u-valign-top u-container-layout-2"><span class="u-icon u-icon-circle u-palette-3-base u-text-palette-1-base u-icon-1"><svg class="u-svg-link" preserveAspectRatio="xMidYMin slice" viewBox="0 0 512.174 512.174" style=""><use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#svg-4105"></use></svg><svg class="u-svg-content" viewBox="0 0 512.174 512.174" id="svg-4105"><g><path d="m497.174 229.244c8.284 0 15-6.716 15-15v-199.04c0-8.284-6.716-15-15-15h-197.403c-8.284 0-15 6.716-15 15v84.521h-57.092v-84.521c0-8.284-6.716-15-15-15h-197.405c-8.284 0-15 6.716-15 15v199.04c0 8.284 6.716 15 15 15h83.702v53.685h-83.976c-8.284 0-15 6.716-15 15v199.04c0 8.284 6.716 15 15 15h197.404c8.284 0 15-6.716 15-15v-84.521h57.366v84.521c0 8.284 6.716 15 15 15h197.403c8.284 0 15-6.716 15-15v-199.04c0-8.284-6.716-15-15-15h-83.702v-53.685zm-182.403-199.04h167.403v169.04h-167.403zm-284.497 0h167.404v169.04h-167.404zm167.13 451.765h-167.404v-169.04h167.404zm284.77 0h-167.403v-169.04h167.403zm-98.702-199.04h-83.701c-8.284 0-15 6.716-15 15v84.52h-57.366v-84.52c0-8.284-6.716-15-15-15h-83.428v-53.685h83.702c8.284 0 15-6.716 15-15v-84.52h57.092v84.52c0 8.284 6.716 15 15 15h83.701z"></path><path d="m128.977 152.277v-22.753h22.877c8.284 0 15-6.716 15-15s-6.716-15-15-15h-22.877v-22.753c0-8.284-6.716-15-15-15s-15 6.716-15 15v22.753h-22.877c-8.284 0-15 6.716-15 15s6.716 15 15 15h22.877v22.753c0 8.284 6.716 15 15 15s15-6.716 15-15z"></path><path d="m382.277 360.13c-5.868-5.848-15.364-5.834-21.213.035-5.849 5.867-5.833 15.364.035 21.213l16.124 16.071-16.123 16.071c-5.868 5.849-5.884 15.346-.035 21.213 2.931 2.94 6.777 4.411 10.624 4.411 3.83 0 7.662-1.458 10.589-4.376l16.194-16.141 16.194 16.141c2.928 2.918 6.758 4.376 10.589 4.376 3.847 0 7.693-1.471 10.624-4.411 5.849-5.867 5.833-15.364-.035-21.213l-16.124-16.071 16.124-16.071c5.868-5.849 5.884-15.346.035-21.213-5.85-5.868-15.347-5.884-21.213-.035l-16.194 16.141z"></path><path d="m151.579 382.449h-75.754c-8.284 0-15 6.716-15 15s6.716 15 15 15h75.754c8.284 0 15-6.716 15-15s-6.716-15-15-15z"></path><path d="m361.064 152.01c2.931 2.94 6.777 4.411 10.624 4.411 3.831 0 7.662-1.458 10.589-4.376l53.566-53.391c5.868-5.848 5.884-15.346.035-21.213-5.851-5.869-15.349-5.882-21.213-.035l-53.565 53.39c-5.869 5.848-5.884 15.346-.036 21.214z"></path><path d="m371.689 103.392c8.512 0 15.413-6.878 15.413-15.362s-6.9-15.362-15.413-15.362c-8.512 0-15.413 6.878-15.413 15.362s6.901 15.362 15.413 15.362z"></path><ellipse cx="425.255" cy="141.42" rx="15.413" ry="15.362"></ellipse>
</g></svg></span>
                <h4 class="u-align-center u-text u-text-palette-1-base u-text-3">Maths</h4>
              </div>
            </div>
            <div class="u-align-center u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-white u-list-item-2">
              <div class="u-container-layout u-similar-container u-valign-top u-container-layout-3"><span class="u-icon u-icon-circle u-palette-3-base u-text-palette-1-base u-icon-2"><svg class="u-svg-link" preserveAspectRatio="xMidYMin slice" viewBox="0 0 508.287 508.287" style=""><use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#svg-9def"></use></svg><svg class="u-svg-content" viewBox="0 0 508.287 508.287" id="svg-9def"><g id="XMLID_987_"><path id="XMLID_990_" d="m491.476 320.353c-6.689-16.251-18.757-33.822-35.864-52.226-4.333-4.661-8.948-9.327-13.815-13.984 4.868-4.657 9.482-9.323 13.815-13.984 17.107-18.403 29.175-35.975 35.864-52.226 9.934-24.127 5.92-40.95.803-50.814-5.535-10.67-16.706-19.559-31.394-25.229-3.969-20.036-21.674-35.192-42.857-35.192-19.579 0-36.191 12.944-41.729 30.724-7.988 1.524-16.368 3.443-25.057 5.73-2.946-11.71-6.278-22.807-9.979-33.16-8.459-23.66-18.501-42.462-29.846-55.884-16.844-19.925-33.625-24.108-44.736-24.108s-27.892 4.183-44.736 24.11c-11.345 13.421-21.387 32.224-29.846 55.884-3.84 10.742-7.279 22.289-10.306 34.487-12.222-2.93-24.056-5.194-35.359-6.732-24.897-3.385-46.212-3.13-63.35.762-25.445 5.776-36.885 18.747-42.001 28.61s-9.13 26.685.803 50.813c6.69 16.251 18.756 33.822 35.864 52.226 4.12 4.432 8.495 8.869 13.1 13.298-25.88 24.432-43.053 48.123-50.339 69.383-17.304 5.817-29.808 22.18-29.808 41.419 0 24.093 19.601 43.694 43.694 43.694 9.87 0 18.983-3.293 26.307-8.834 10.001 2.645 21.517 3.939 34.276 3.939 19.674 0 42.305-3.082 66.872-9.009 3.012 12.108 6.431 23.573 10.246 34.243 8.459 23.66 18.501 42.462 29.846 55.884 16.844 19.927 33.625 24.11 44.736 24.11 14.605 0 26.998-5.398 38.343-16.832 3.337.818 6.82 1.262 10.405 1.262 24.093 0 43.694-19.601 43.694-43.694 0-12.627-5.39-24.014-13.983-31.999 2.406-7.411 4.621-15.14 6.644-23.166 12.146 2.905 23.907 5.152 35.144 6.68 11.58 1.574 22.381 2.361 32.351 2.361 11.467 0 21.832-1.041 31-3.123 25.444-5.776 36.885-18.747 42.001-28.61s9.131-26.686-.803-50.813zm-73.448-213.654c7.551 0 13.694 6.143 13.694 13.694s-6.144 13.694-13.694 13.694-13.694-6.143-13.694-13.694 6.143-13.694 13.694-13.694zm-40.123 30.978c6.711 15.52 22.167 26.411 40.123 26.411 16.049 0 30.096-8.704 37.693-21.633 5.197 2.775 8.585 5.891 9.928 8.48 7.841 15.117-7.858 46.826-46.35 83.251-16.414-13.564-34.823-26.867-54.719-39.547-1.612-18.094-3.962-35.571-7.003-52.158 7.016-1.865 13.808-3.472 20.328-4.804zm-78.762 179.048c-11.072 5.743-21.895 10.99-32.437 15.77-10.574-4.781-21.413-10.025-32.488-15.769-12.985-6.736-25.222-13.602-36.727-20.527-.85-13.401-1.31-27.427-1.31-42.055 0-14.665.463-28.725 1.316-42.157 11.745-7.004 24.013-13.833 36.721-20.425 10.725-5.563 21.577-10.834 32.418-15.772 10.582 4.784 21.424 10.023 32.507 15.772 12.985 6.736 25.223 13.603 36.728 20.528.85 13.401 1.31 27.427 1.31 42.054 0 14.415-.422 28.441-1.249 42.017-11.522 6.937-23.781 13.817-36.789 20.564zm33.437 16.043c-1.012 8.133-2.191 16.048-3.529 23.736-8.085-2.543-16.433-5.407-25.021-8.604 2.972-1.49 5.947-2.997 8.927-4.543 6.646-3.448 13.188-6.984 19.623-10.589zm-103.158 15.176c-8.555 3.203-16.862 6.07-24.899 8.617-1.33-7.589-2.528-15.491-3.572-23.699 6.381 3.573 12.866 7.077 19.453 10.494 3.004 1.558 6.011 3.083 9.018 4.588zm-62.884-71.7c-10.91-7.544-20.94-15.076-30.096-22.507 9.37-7.434 19.433-14.809 30.107-22.065-.241 7.431-.369 14.925-.369 22.471.001 7.422.125 14.792.358 22.101zm34.419-100.861c1.037-8.151 2.226-15.999 3.546-23.539 8.023 2.528 16.307 5.372 24.826 8.544-2.983 1.495-5.959 3.006-8.923 4.544-6.597 3.421-13.081 6.909-19.449 10.451zm102.72-15.172c8.488-3.272 16.866-6.292 25.067-9.036 1.369 7.756 2.598 15.844 3.667 24.25-6.381-3.573-12.866-7.077-19.453-10.494-3.092-1.603-6.186-3.173-9.281-4.72zm63.146 71.832c10.71 7.407 20.575 14.801 29.595 22.1-9.013 7.293-18.868 14.681-29.568 22.081.216-7.265.33-14.624.33-22.081.001-7.42-.123-14.79-.357-22.1zm-100.142-202.043c18.345 0 41.201 33.117 55.824 91.678-18.082 5.929-36.96 13.125-55.963 21.347-18.959-8.074-37.711-14.99-55.871-20.603 14.614-59.026 37.588-92.422 56.01-92.422zm-198.968 120.935c5.066-9.768 21.447-15.489 46.425-15.489 16.841 0 37.593 2.609 61.406 8.33-2.912 16.121-5.171 33.074-6.74 50.605-20.217 12.699-38.797 25.899-55.282 39.289-38.094-36.208-53.613-67.69-45.809-82.735zm-13.316 227.019c-7.551 0-13.694-6.143-13.694-13.694s6.143-13.694 13.694-13.694 13.695 6.143 13.695 13.694-6.143 13.694-13.695 13.694zm43.014-6.061c.439-2.481.681-5.029.681-7.633 0-17.732-10.624-33.02-25.835-39.862 7.339-15.131 21.435-32.647 41.085-50.898 16.597 13.772 35.249 27.282 55.439 40.148 1.576 17.683 3.852 34.781 6.793 51.031-32.729 7.914-59.467 9.841-78.163 7.214zm218.018 90.824c-7.551 0-13.694-6.143-13.694-13.694s6.144-13.694 13.694-13.694 13.694 6.143 13.694 13.694-6.143 13.694-13.694 13.694zm1.952-57.339c-.648-.029-1.297-.049-1.951-.049-24.093 0-43.694 19.601-43.694 43.694 0 9.289 2.922 17.903 7.883 24.99-4.528 3.385-8.558 4.274-12.937 4.274-18.404 0-41.35-33.326-55.966-92.24 18.038-5.619 36.83-12.584 56.037-20.815 19.041 8.111 37.873 15.055 56.107 20.684-1.685 6.725-3.509 13.222-5.479 19.462zm148.268-48.025c-8.47 16.33-48.589 21.355-107.576 7.225 2.908-16.131 5.133-33.19 6.657-51.023 19.839-12.651 38.197-25.922 54.57-39.453 38.491 36.424 54.19 68.134 46.349 83.251z"></path><path id="XMLID_1506_" d="m266.681 208.644c-25.089 0-45.5 20.411-45.5 45.5s20.412 45.5 45.5 45.5 45.5-20.411 45.5-45.5-20.411-45.5-45.5-45.5zm0 61c-8.547 0-15.5-6.953-15.5-15.5s6.954-15.5 15.5-15.5 15.5 6.953 15.5 15.5-6.953 15.5-15.5 15.5z"></path>
</g></svg></span>
                <h4 class="u-align-center-sm u-align-center-xs u-text u-text-palette-1-base u-text-4">Physics</h4>
              </div>
            </div>
            <div class="u-align-center u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-white u-list-item-3">
              <div class="u-container-layout u-similar-container u-valign-top u-container-layout-4"><span class="u-file-icon u-icon u-icon-circle u-palette-3-base u-text-palette-1-base u-icon-3"><img src="images/840781-6ced8a49.png" alt=""></span>
                <h4 class="u-align-center-sm u-align-center-xs u-text u-text-palette-1-base u-text-5"> Medicine</h4>
              </div>
            </div>
            <div class="u-align-center u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-white u-list-item-4">
              <div class="u-container-layout u-similar-container u-valign-top u-container-layout-5"><span class="u-icon u-icon-circle u-palette-3-base u-text-palette-1-base u-icon-4"><svg class="u-svg-link" preserveAspectRatio="xMidYMin slice" viewBox="0 -41 512 512" style=""><use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#svg-6443"></use></svg><svg class="u-svg-content" viewBox="0 -41 512 512" id="svg-6443"><path d="m407 0h-302c-57.898438 0-105 47.101562-105 105v168.945312c0 57.898438 47.101562 105 105 105h15.582031l36.519531 46.332032c2.847657 3.609375 7.1875 5.714844 11.78125 5.714844s8.9375-2.105469 11.78125-5.714844l36.519532-46.332032h189.816406c57.898438 0 105-47.101562 105-105v-168.945312c0-57.898438-47.101562-105-105-105zm-124.757812 230.734375v118.210937h-52.484376v-118.210937c0-8.285156-6.714843-15-15-15h-184.757812v-52.484375h184.757812c8.285157 0 15-6.714844 15-15v-118.25h52.484376v118.25c0 8.285156 6.714843 15 15 15h184.757812v52.484375h-184.757812c-8.285157 0-15 6.714844-15 15zm30-200.734375h82.039062l-82.039062 82.039062zm-112.484376 82.039062-82.039062-82.039062h82.039062zm112.484376 154.910157 81.996093 81.996093h-81.996093zm169.757812-161.949219v28.25h-148.546875l98.851563-98.847656c28.9375 10.40625 49.695312 38.117187 49.695312 70.597656zm-402.304688-70.597656 98.851563 98.847656h-148.546875v-28.25c0-32.480469 20.757812-60.191406 49.695312-70.597656zm-49.695312 239.542968v-28.210937h148.546875l-98.820313 98.820313c-28.957031-10.398438-49.726562-38.117188-49.726562-70.609376zm168.128906 80.714844-29.246094 37.101563-29.242187-37.101563c-2.847656-3.609375-7.1875-5.714844-11.78125-5.714844h-10.097656l81.996093-81.996093v85.984375c-.578124.53125-1.136718 1.097656-1.628906 1.726562zm234.144532-10.105468-98.820313-98.820313h148.546875v28.210937c0 32.492188-20.769531 60.210938-49.726562 70.609376zm0 0"></path></svg></span>
                <h4 class="u-align-center-sm u-align-center-xs u-text u-text-palette-1-base u-text-6">English</h4>
              </div>
            </div>
            <div class="u-align-center u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-white u-list-item-5">
              <div class="u-container-layout u-similar-container u-valign-top u-container-layout-6"><span class="u-file-icon u-icon u-icon-circle u-palette-3-base u-text-palette-1-base u-icon-5"><img src="images/4457024-0e170e4c.png" alt=""></span>
                <h4 class="u-align-center-sm u-align-center-xs u-text u-text-palette-1-base u-text-7"> Technology</h4>
              </div>
            </div>
            <div class="u-align-center u-container-style u-list-item u-radius-20 u-repeater-item u-shape-round u-video-cover u-white u-list-item-6">
              <div class="u-container-layout u-similar-container u-valign-top u-container-layout-7"><span class="u-file-icon u-icon u-icon-circle u-palette-3-base u-text-palette-1-base u-icon-6"><img src="images/6646730-387c719a.png" alt=""></span>
                <h4 class="u-align-center-sm u-align-center-xs u-text u-text-palette-1-base u-text-8"> Engineering</h4>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="u-clearfix u-section-7" id="carousel_33aa">
      <div class="u-clearfix u-sheet u-valign-middle u-sheet-1">
        <div class="u-clearfix u-expanded-width-md u-expanded-width-sm u-expanded-width-xs u-layout-wrap u-layout-wrap-1">
          <div class="u-layout">
            <div class="u-layout-row">
              <div class="u-align-left u-container-style u-layout-cell u-left-cell u-size-15 u-size-60-md u-layout-cell-1">
                <div class="u-container-layout u-container-layout-1">
                  <p class="u-text u-text-1"> The digital library is available 24/7 to our community.</p>
                  <a href="https://nicepage.cloud" class="u-border-none u-btn u-btn-round u-button-style u-palette-3-base u-radius-10 u-text-palette-1-base u-btn-1" data-animation-name="rollIn" data-animation-duration="1000" data-animation-direction="" data-animation-delay="500">learn more</a>
                  <p class="u-text u-text-default u-text-2">Image from <a href="https://www.freepik.com/psd/woman" class="u-border-1 u-border-active-palette-1-base u-border-black u-border-hover-palette-1-base u-btn u-button-link u-button-style u-none u-text-body-color u-btn-2">Freepik</a>
                  </p>
                </div>
              </div>
              <div class="u-align-left u-container-style u-layout-cell u-size-18-lg u-size-18-xl u-size-21-sm u-size-21-xs u-size-60-md u-layout-cell-2">
                <div class="u-container-layout u-container-layout-2"><span class="u-align-left u-icon u-text-palette-3-base u-icon-1"><svg class="u-svg-link" preserveAspectRatio="xMidYMin slice" viewBox="0 0 95.333 95.332" style=""><use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#svg-41ae"></use></svg><svg class="u-svg-content" viewBox="0 0 95.333 95.332" x="0px" y="0px" id="svg-41ae"><g><g><path d="M30.512,43.939c-2.348-0.676-4.696-1.019-6.98-1.019c-3.527,0-6.47,0.806-8.752,1.793    c2.2-8.054,7.485-21.951,18.013-23.516c0.975-0.145,1.774-0.85,2.04-1.799l2.301-8.23c0.194-0.696,0.079-1.441-0.318-2.045    s-1.035-1.007-1.75-1.105c-0.777-0.106-1.569-0.16-2.354-0.16c-12.637,0-25.152,13.19-30.433,32.076    c-3.1,11.08-4.009,27.738,3.627,38.223c4.273,5.867,10.507,9,18.529,9.313c0.033,0.001,0.065,0.002,0.098,0.002    c9.898,0,18.675-6.666,21.345-16.209c1.595-5.705,0.874-11.688-2.032-16.851C40.971,49.307,36.236,45.586,30.512,43.939z"></path><path d="M92.471,54.413c-2.875-5.106-7.61-8.827-13.334-10.474c-2.348-0.676-4.696-1.019-6.979-1.019    c-3.527,0-6.471,0.806-8.753,1.793c2.2-8.054,7.485-21.951,18.014-23.516c0.975-0.145,1.773-0.85,2.04-1.799l2.301-8.23    c0.194-0.696,0.079-1.441-0.318-2.045c-0.396-0.604-1.034-1.007-1.75-1.105c-0.776-0.106-1.568-0.16-2.354-0.16    c-12.637,0-25.152,13.19-30.434,32.076c-3.099,11.08-4.008,27.738,3.629,38.225c4.272,5.866,10.507,9,18.528,9.312    c0.033,0.001,0.065,0.002,0.099,0.002c9.897,0,18.675-6.666,21.345-16.209C96.098,65.559,95.376,59.575,92.471,54.413z"></path>
</g>
</g></svg></span><span class="u-file-icon u-icon u-palette-3-base u-text-palette-1-base u-icon-2"><img src="images/1633659-c312dd2d.png" alt=""></span>
                  <p class="u-text u-text-3"> This place has given me so much that I am only too happy to be allowed to help it to develop and to be able to give back to it a fraction of what it has given to me...</p>
                  <h4 class="u-text u-text-palette-5-base u-text-4"> Sally Hamstead<span style="font-size: 0.875rem;"></span>
                  </h4>
                </div>
              </div>
              <div class="u-align-center-sm u-align-center-xs u-container-style u-layout-cell u-right-cell u-size-24-sm u-size-24-xs u-size-27-lg u-size-27-xl u-size-60-md u-layout-cell-3">
                <div class="u-container-layout u-valign-middle-md u-container-layout-3">
                  <div class="u-expanded-width u-gradient u-shape u-shape-rectangle u-shape-1"></div>
                  <img src="images/ggg.jpg" alt="" class="u-align-left u-image u-image-default u-image-1" data-image-width="900" data-image-height="946">
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="u-align-center u-clearfix u-grey-5 u-section-8" id="carousel_6405">
      <div class="u-clearfix u-sheet u-valign-middle u-sheet-1">
        <div class="u-clearfix u-expanded-width u-gutter-20 u-layout-wrap u-layout-wrap-1">
          <div class="u-layout">
            <div class="u-layout-row">
              <div class="u-align-center u-container-style u-layout-cell u-size-38 u-layout-cell-1">
                <div class="u-container-layout u-valign-middle-lg u-valign-middle-md u-valign-middle-xl u-container-layout-1">
                  <div class="u-form u-form-1">
                    <form action="//publish.nicepage.com/Form/Process" method="POST" class="u-clearfix u-form-spacing-15 u-form-vertical u-inner-form" style="padding: 0;" source="email" name="form">
                      <div class="u-form-email u-form-group u-form-partition-factor-2">
                        <label for="email-f2a8" class="u-label u-label-1">E-mail</label>
                        <input type="email" placeholder="Enter a valid email address" id="email-f2a8" name="email" class="u-border-2 u-border-grey-75 u-border-no-left u-border-no-right u-border-no-top u-input u-input-rectangle" required="">
                      </div>
                      <div class="u-form-group u-form-name u-form-partition-factor-2">
                        <label for="name-f2a8" class="u-label u-label-2">Name</label>
                        <input type="text" placeholder="Enter your Name" id="name-f2a8" name="name" class="u-border-2 u-border-grey-75 u-border-no-left u-border-no-right u-border-no-top u-input u-input-rectangle" required="">
                      </div>
                      <div class="u-form-group u-form-select u-form-group-3">
                        <label for="select-8e9d" class="u-form-control-hidden u-label u-label-3">Select</label>
                        <div class="u-form-select-wrapper">
                          <select id="select-8e9d" name="select" class="u-border-2 u-border-grey-75 u-border-no-left u-border-no-right u-border-no-top u-input u-input-rectangle">
                            <option value="Item 1">Item 1</option>
                            <option value="Item 2">Item 2</option>
                            <option value="Item 3">Item 3</option>
                          </select>
                          <svg xmlns="http://www.w3.org/2000/svg" width="14" height="12" version="1" class="u-caret"><path fill="currentColor" d="M4 8L0 4h8z"></path></svg>
                        </div>
                      </div>
                      <div class="u-form-date u-form-group u-form-partition-factor-2 u-form-group-4">
                        <label for="date-4441" class="u-label u-label-4">Date</label>
                        <input type="date" placeholder="MM/DD/YYYY" id="date-4441" name="date" class="u-border-2 u-border-grey-75 u-border-no-left u-border-no-right u-border-no-top u-input u-input-rectangle" required="">
                      </div>
                      <div class="u-form-group u-form-partition-factor-2 u-form-phone u-form-group-5">
                        <label for="phone-447e" class="u-label u-label-5">Phone</label>
                        <input type="tel" pattern="\+?\d{0,2}[\s\(\-]?([0-9]{3})[\s\)\-]?([\s\-]?)([0-9]{3})[\s\-]?([0-9]{2})[\s\-]?([0-9]{2})" placeholder="Enter your phone (e.g. +14155552675)" id="phone-447e" name="phone" class="u-border-2 u-border-grey-75 u-border-no-left u-border-no-right u-border-no-top u-input u-input-rectangle" required="">
                      </div>
                      <div class="u-form-group u-form-message u-form-group-6">
                        <label for="message-f2a8" class="u-label u-label-6">Message</label>
                        <textarea placeholder="Enter your message" rows="4" cols="50" id="message-f2a8" name="message" class="u-border-2 u-border-grey-75 u-border-no-left u-border-no-right u-border-no-top u-input u-input-rectangle" required=""></textarea>
                      </div>
                      <div class="u-align-left u-form-group u-form-submit">
                        <a href="#" class="u-active-palette-1-base u-border-none u-btn u-btn-rectangle u-btn-submit u-button-style u-hover-palette-1-base u-palette-3-base u-text-active-white u-text-hover-white u-text-palette-1-base u-btn-1">Submit</a>
                        <input type="submit" value="submit" class="u-form-control-hidden">
                      </div>
                      <div class="u-form-send-message u-form-send-success"> Thank you! Your message has been sent. </div>
                      <div class="u-form-send-error u-form-send-message"> Unable to send your message. Please fix errors then try again. </div>
                      <input type="hidden" value="" name="recaptchaResponse">
                    </form>
                  </div>
                </div>
              </div>
              <div class="u-container-style u-layout-cell u-size-22 u-white u-layout-cell-2">
                <div class="u-container-layout u-valign-middle u-container-layout-2">
                  <p class="u-text u-text-default u-text-1"> Welcome to our world-class library, right in your backyard. We bring you the most diverse collection of physical and digital resources across a variety of faculties. Each level of the library is easily accessible to students and members. We offer advanced digital services, e-books, e-journals, and the useful Library repository. In addition to research support throughout the research journey, our staff and librarians are equipped to service and aid any research query, no matter the discipline or field.&nbsp;</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>


    <footer class="u-align-center u-clearfix u-footer u-grey-80 u-footer" id="sec-90c0"><div class="u-clearfix u-sheet u-sheet-1">
        <p class="u-small-text u-text u-text-variant u-text-1">Offensive Security</p>
      </div></footer>
    <section class="u-backlink u-clearfix u-grey-80">
      <a class="u-link" href="https://nicepage.com/website-design" target="_blank">
        <span>Website Design Ideas</span>
      </a>
      <p class="u-text">
        <span>created with</span>
      </p>
      <a class="u-link" href="https://nicepage.one" target="_blank">
        <span>Best Website Builder</span>
      </a>.
    </section>

</body></html>

```
# curl - robots

```

```

# enumeration
