# nmap 

```
# Nmap 7.95 scan initiated Sun Jun  8 04:24:48 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/tcp80/tcp_80_http_nmap.txt -oX /home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/tcp80/xml/tcp_80_http_nmap.xml 192.168.143.163
Nmap scan report for exfiltrated.offsec (192.168.143.163)
Host is up, received user-set (0.037s latency).
Scanned at 2025-06-08 04:24:49 EDT for 114s

PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.41 ((Ubuntu))
|_http-server-header: Apache/2.4.41 (Ubuntu)
| http-robots.txt: 7 disallowed entries 
| /backup/ /cron/? /front/ /install/ /panel/ /tmp/ 
|_/updates/
|_http-date: Sun, 08 Jun 2025 08:24:59 GMT; -1s from local time.
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
| http-referer-checker: 
| Spidering limited to: maxpagecount=30
|   https://oss.maxcdn.com:443/respond/1.4.2/respond.min.js
|_  https://oss.maxcdn.com:443/html5shiv/3.7.2/html5shiv.min.js
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-feed: Couldn't find any feeds.
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
| http-headers: 
|   Date: Sun, 08 Jun 2025 08:24:58 GMT
|   Server: Apache/2.4.41 (Ubuntu)
|   Set-Cookie: INTELLI_06c8042c3d=f8s3vqrcuodk6s8r1gino5mlq8; path=/
|   Expires: Thu, 19 Nov 1981 08:52:00 GMT
|   Cache-Control: no-store, no-cache, must-revalidate
|   Pragma: no-cache
|   Set-Cookie: INTELLI_06c8042c3d=f8s3vqrcuodk6s8r1gino5mlq8; expires=Sun, 08-Jun-2025 08:54:58 GMT; Max-Age=1800; path=/
|   X-Powered-CMS: Subrion CMS
|   Connection: close
|   Content-Type: text/html;charset=UTF-8
|   
|_  (Request type: HEAD)
|_http-traceroute: ERROR: Script execution failed (use -d to debug)
|_http-favicon: Unknown favicon MD5: 09BDDB30D6AE11E854BFF82ED638542B
|_http-fetch: Please enter the complete path of the directory to save data in.
| http-php-version: Logo query returned unknown hash e0c8dd27ccda1dfe6d0843d639f05552
|_Credits query returned unknown hash 3bf5669b4738c14da48f871a5f2a4bbe
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-grep: 
|   (2) http://exfiltrated.offsec:80/modules/fancybox/js/jquery.fancybox.css?fm=1528952694: 
|     (2) email: 
|       + sprite@2x.png
|_      + loading@2x.gif
|_http-dombased-xss: Couldn't find any DOM based XSS.
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=exfiltrated.offsec
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://exfiltrated.offsec:80/
|     Form id: 
|     Form action: http://exfiltrated.offsec/search/
|     
|     Path: http://exfiltrated.offsec:80/terms/
|     Form id: 
|     Form action: http://exfiltrated.offsec/search/
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Form id: 
|     Form action: http://exfiltrated.offsec/search/
|     
|     Path: http://exfiltrated.offsec:80/about/
|     Form id: 
|     Form action: http://exfiltrated.offsec/search/
|     
|     Path: http://exfiltrated.offsec:80/login/
|     Form id: 
|     Form action: http://exfiltrated.offsec/search/
|     
|     Path: http://exfiltrated.offsec:80/login/
|     Form id: 
|     Form action: http://exfiltrated.offsec/login/
|     
|     Path: http://exfiltrated.offsec:80/help/
|     Form id: 
|_    Form action: http://exfiltrated.offsec/search/
|_http-generator: Subrion CMS - Open Source Content Management System
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
|_http-errors: Couldn't find any error pages.
|_http-malware-host: Host appears to be clean
| http-security-headers: 
|   Cache_Control: 
|     Header: Cache-Control: no-store, no-cache, must-revalidate
|   Pragma: 
|     Header: Pragma: no-cache
|   Expires: 
|_    Header: Expires: Thu, 19 Nov 1981 08:52:00 GMT
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=exfiltrated.offsec
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Line number: 204
|     Comment: 
|         <!--__e_c_-->
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Line number: 73
|     Comment: 
|         <!-- MORE menu dropdown -->
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Line number: 466
|     Comment: 
|         <!-- SYSTEM STUFF -->
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Line number: 19
|     Comment: 
|         <!--[if lt IE 9]>
|                     <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
|                     <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
|                 <![endif]-->
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Line number: 18
|     Comment: 
|         <!-- HTML5 shim and Respond.js IE8 support of HTML5 elements and media queries -->
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Line number: 192
|     Comment: 
|         <!--__b_-->
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Line number: 209
|     Comment: 
|         <!--__e_-->
|     
|     Path: http://exfiltrated.offsec:80/policy/
|     Line number: 199
|     Comment: 
|_        <!--__b_c_-->
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-chrono: Request times for /; avg: 300.15ms; min: 220.01ms; max: 348.81ms
| http-vhosts: 
| test.offsec
| http.offsec
| devtest.offsec
| cdn.offsec
| noc.offsec
| ssl.offsec
| sql.offsec
| ntp.offsec
| devsql.offsec
|_119 names had status 302
|_http-title: Home :: Powered by Subrion 4.2
|_http-mobileversion-checker: No mobile version detected.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1; ico: 1
|     /modules/fancybox/js/
|       css: 1; js: 1
|     /policy/
|       Other: 1
|     /templates/kickstart/css/
|       css: 1
|     /templates/kickstart/img/
|       png: 2
|     /templates/kickstart/js/
|       js: 1
|     /terms/
|       Other: 1
|   Longest directory structure:
|     Depth: 3
|     Dir: /templates/kickstart/img/
|   Total files found (by extension):
|_    Other: 3; css: 2; ico: 1; js: 2; png: 2
|_http-config-backup: ERROR: Script execution failed (use -d to debug)
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
| http-sql-injection: 
|   Possible sqli for queries:
|     http://exfiltrated.offsec:80/tmp/cache/%5C%22?manage_exit=y%5C%22%27%20OR%20sqlspider
|_    http://exfiltrated.offsec:80/tmp/cache/%5C%22?preview_exit=y%5C%22%27%20OR%20sqlspider
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-enum: 
|   /blog/: Blog
|   /clientaccesspolicy.xml: Microsoft Silverlight crossdomain policy
|   /atom.xml: RSS or Atom feed
|   /rss.xml: RSS or Atom feed
|   /login/: Login page
|   /robots.txt: Robots file
|   /crossdomain.xml: Adobe Flash crossdomain policy
|   /.gitignore: Revision control ignore file
|   /Citrix/PNAgent/config.xml: Citrix
|   /changelog.txt: Version field
|   /admin/environment.xml: Moodle files
|   /manifest.json: Manifest JSON File
|   /0/: Potentially interesting folder
|   /cron/: Potentially interesting folder
|   /help/: Potentially interesting folder
|   /index/: Potentially interesting folder
|   /members/: Potentially interesting folder
|   /search/: Potentially interesting folder
|   /sitecore/shell/sitecore.version.xml: Sitecore.NET login page
|   /sitecore/shell/Applications/shell.xml: Sitecore.NET (CMS)
|   /App_Config/Security/Domains.config.xml: Sitecore.NET (CMS)
|_  /App_Config/Security/GlobalRoles.config.xml: Sitecore.NET (CMS)

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Jun  8 04:26:43 2025 -- 1 IP address (1 host up) scanned in 114.52 seconds

```

# nikto 

```
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          192.168.143.163
+ Target Hostname:    192.168.143.163
+ Target Port:        80
+ Start Time:         2025-06-08 04:24:53 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.41 (Ubuntu)
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ /: Cookie INTELLI_06c8042c3d created without the httponly flag. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies
+ Root page / redirects to: http://exfiltrated.offsec/
+ All CGI directories 'found', use '-C none' to test none
+ /robots.txt: Entry '/panel/' is returned a non-forbidden or redirect HTTP code (200). See: https://portswigger.net/kb/issues/00600600_robots-txt-file
+ /robots.txt: contains 7 entries which should be manually viewed. See: https://developer.mozilla.org/en-US/docs/Glossary/Robots.txt
+ Apache/2.4.41 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.
+ /sitemap.xml: This gives a nice listing of the site content.
+ /license.txt: License file found may identify site software.
+ /panel/: Admin login page/section found.
+ /.gitignore: .gitignore file found. It is possible to grasp the directory structure.
+ http://169.254.169.254/metadata/instance?api-version=2017-08-01: The Azure host is configured as a reverse proxy which allows access to the Meta-Data service. This could allow significant access to the host/infrastructure.
+ /README.md: Readme Found.
+ http://aws.cirt.net/metadata/instance?api-version=2017-08-01: The Azure host is configured as a reverse proxy which allows access to the Meta-Data service. This could allow significant access to the host/infrastructure.
+ 24940 requests: 0 error(s) and 13 item(s) reported on remote host
+ End Time:           2025-06-08 04:31:41 (GMT-4) (408 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested


```

# screenshot


# whatweb

```
WhatWeb report for http://192.168.143.163:80
Status    : 302 Found
Title     : <None>
IP        : 192.168.143.163
Country   : RESERVED, ZZ

Summary   : Apache[2.4.41], Cookies[INTELLI_06c8042c3d], HTTPServer[Ubuntu Linux][Apache/2.4.41 (Ubuntu)], RedirectLocation[http://exfiltrated.offsec/]

Detected Plugins:
[ Apache ]
	The Apache HTTP Server Project is an effort to develop and
	maintain an open-source HTTP server for modern operating
	systems including UNIX and Windows NT. The goal of this
	project is to provide a secure, efficient and extensible
	server that provides HTTP services in sync with the current
	HTTP standards.

	Version      : 2.4.41 (from HTTP Server Header)
	Google Dorks: (3)
	Website     : http://httpd.apache.org/

[ Cookies ]
	Display the names of cookies in the HTTP headers. The
	values are not returned to save on space.

	String       : INTELLI_06c8042c3d
	String       : INTELLI_06c8042c3d

[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	OS           : Ubuntu Linux
	String       : Apache/2.4.41 (Ubuntu) (from server string)

[ RedirectLocation ]
	HTTP Server string location. used with http-status 301 and
	302

	String       : http://exfiltrated.offsec/ (from location)

HTTP Headers:
	HTTP/1.1 302 Found
	Date: Sun, 08 Jun 2025 08:24:52 GMT
	Server: Apache/2.4.41 (Ubuntu)
	Set-Cookie: INTELLI_06c8042c3d=mkbsrnbhtes7d284go8ip15v5m; path=/
	Expires: Thu, 19 Nov 1981 08:52:00 GMT
	Cache-Control: no-store, no-cache, must-revalidate
	Pragma: no-cache
	Set-Cookie: INTELLI_06c8042c3d=mkbsrnbhtes7d284go8ip15v5m; expires=Sun, 08-Jun-2025 08:54:52 GMT; Max-Age=1800; path=/
	Location: http://exfiltrated.offsec/
	Content-Length: 0
	Connection: close
	Content-Type: text/html; charset=UTF-8



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
    target_url: "http://192.168.143.163:80/",
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
    output: "/home/kali/OSCP/pg/exfiltrated/results/192.168.143.163/scans/tcp80/tcp_80_http_feroxbuster_dirbuster.txt",
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
403      GET        9l       28w      280c http://192.168.143.163/updates
200      GET        1l        1w       53c http://exfiltrated.offsec/cron/?/
404      GET      467l      749w    17492c http://exfiltrated.offsec/backup/
404      GET      467l      749w    17489c http://exfiltrated.offsec/tmp/
404      GET      467l      749w    17491c http://exfiltrated.offsec/front/
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/templates/kickstart/img/browser.png
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/tmp/cache/intelli.config.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.css
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/templates/kickstart/js/app.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/js/bootstrap/js/bootstrap.min.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.pack.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/templates/kickstart/css/user-style.css
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/js/intelli/intelli.minmax.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/js/frontend/footer.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/templates/kickstart/img/computer2.png
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/templates/kickstart/img/computer.png
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/templates/kickstart/css/iabootstrap.css
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/js/jquery/jquery.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/js/intelli/intelli.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/templates/kickstart/img/logo.png
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/tmp/cache/intelli.lang.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/exfiltrated.offsec/favicon.ico
200      GET      580l     1219w    21687c http://exfiltrated.offsec/
200      GET       17l       17w      247c http://192.168.143.163/.gitignore
404      GET        9l       31w      277c http://192.168.143.163/.swf
200      GET        1l        4w       76c http://exfiltrated.offsec/.well-known/assetlinks.json
200      GET        1l        4w       76c http://exfiltrated.offsec/.well-known/host-meta.json
200      GET        1l        4w       76c http://exfiltrated.offsec/.well-known/jwks.json
200      GET      580l     1219w    21687c http://exfiltrated.offsec/0
200      GET        0l        0w        0c http://exfiltrated.offsec/actions/
200      GET        0l        0w        0c http://exfiltrated.offsec/actions.txt
200      GET        0l        0w        0c http://exfiltrated.offsec/actions.html
200      GET        0l        0w        0c http://exfiltrated.offsec/actions.php
200      GET        0l        0w        0c http://exfiltrated.offsec/actions.asp
200      GET        0l        0w        0c http://exfiltrated.offsec/actions.aspx
200      GET        0l        0w        0c http://exfiltrated.offsec/actions.jsp
200      GET       24l       50w     2909c http://exfiltrated.offsec/captcha/
200      GET      913l     7748w    49250c http://192.168.143.163/changelog.txt
200      GET        1l        1w       53c http://exfiltrated.offsec/cron/
200      GET        1l        1w       53c http://exfiltrated.offsec/cron.txt
200      GET        1l        1w       53c http://exfiltrated.offsec/cron.html
200      GET        1l        1w       53c http://exfiltrated.offsec/cron.php
200      GET        1l        1w       53c http://exfiltrated.offsec/cron.asp
200      GET        1l        1w       53c http://exfiltrated.offsec/cron.aspx
200      GET        1l        1w       53c http://exfiltrated.offsec/cron.jsp
200      GET        2l        6w      104c http://exfiltrated.offsec/crossdomain.xml
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/templates/kickstart/img/computer.png
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.pack.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/js/intelli/intelli.minmax.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.css
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/js/bootstrap/js/bootstrap.min.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/templates/kickstart/img/logo.png
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/js/intelli/intelli.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/templates/kickstart/css/user-style.css
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/js/jquery/jquery.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/favicon.ico
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/js/frontend/footer.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/templates/kickstart/css/iabootstrap.css
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/tmp/cache/intelli.lang.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/templates/kickstart/img/browser.png
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/tmp/cache/intelli.config.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/templates/kickstart/js/app.js
404      GET        9l       31w      280c http://exfiltrated.offsec/en/exfiltrated.offsec/templates/kickstart/img/computer2.png
200      GET      580l     1219w    21687c http://exfiltrated.offsec/en/
200      GET        4l       24w     2340c http://192.168.143.163/favicon.ico
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/templates/kickstart/img/computer.png
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/templates/kickstart/css/user-style.css
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/js/intelli/intelli.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/js/intelli/intelli.minmax.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/templates/kickstart/img/browser.png
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/tmp/cache/intelli.lang.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/templates/kickstart/css/iabootstrap.css
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/templates/kickstart/img/logo.png
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/tmp/cache/intelli.config.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.pack.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/templates/kickstart/img/computer2.png
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/favicon.ico
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/js/frontend/footer.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/templates/kickstart/js/app.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/js/bootstrap/js/bootstrap.min.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/js/jquery/jquery.js
404      GET        9l       31w      280c http://exfiltrated.offsec/index/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.css
200      GET      580l     1219w    21693c http://exfiltrated.offsec/index/
200      GET      580l     1219w    21693c http://exfiltrated.offsec/index.php
403      GET        1l        1w       10c http://192.168.143.163/install/
200      GET      674l     5644w    35147c http://192.168.143.163/license.txt
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/js/frontend/footer.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/templates/kickstart/js/app.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/tmp/cache/intelli.lang.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/js/frontend/search.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/js/jquery/jquery.js
200      GET        1l        1w        2c http://exfiltrated.offsec/members/search/member.json
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/templates/kickstart/css/user-style.css
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/templates/kickstart/css/iabootstrap.css
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.css
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/js/intelli/intelli.minmax.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.pack.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/templates/kickstart/img/logo.png
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/tmp/cache/intelli.config.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/js/intelli/intelli.search.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/js/intelli/intelli.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/favicon.ico
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/js/bootstrap/js/bootstrap.min.js
404      GET        9l       31w      280c http://exfiltrated.offsec/members/exfiltrated.offsec/js/jquery/plugins/select2/select2.min.js
200      GET      611l     1032w    25371c http://exfiltrated.offsec/members/exfiltrated.offsec/cron
200      GET      611l     1032w    25299c http://exfiltrated.offsec/members/
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/bootstrap/css/passfield.css
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/admin/templates/default/css/bootstrap-default.css
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/admin/templates/default/img/ico/apple-touch-icon-72-precomposed.png
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/tmp/cache/intelli.config.en.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/bootstrap/js/bootstrap-switch.min.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/admin/templates/default/img/ico/apple-touch-icon-57-precomposed.png
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/admin/templates/default/img/subrion-logo-lines.png
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/intelli/intelli.admin.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/admin/templates/default/img/ico/apple-touch-icon-114-precomposed.png
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/admin/footer.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/admin/templates/default/img/ico/favicon.ico
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/admin/templates/default/js/bootstrap.min.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/tmp/cache/intelli.admin.lang.en.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/bootstrap/js/passfield.min.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/jquery/jquery.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/admin/templates/default/img/ico/apple-touch-icon-144-precomposed.png
200      GET        6l      109w     4034c http://192.168.143.163/js/utils/respond.min.js
200      GET        8l       70w     2376c http://192.168.143.163/js/utils/shiv.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/admin/login.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/bootstrap/js/fontawesome-iconpicker.min.js
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/bootstrap/css/fontawesome-iconpicker.min.css
404      GET        9l       31w      277c http://192.168.143.163/panel/192.168.143.163/js/intelli/intelli.js
200      GET      107l      259w     6091c http://192.168.143.163/panel/
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/admin/templates/default/js/bootstrap.min.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/admin/templates/default/img/ico/apple-touch-icon-57-precomposed.png
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/bootstrap/js/passfield.min.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/bootstrap/js/fontawesome-iconpicker.min.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/intelli/intelli.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/admin/templates/default/img/ico/favicon.ico
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/intelli/intelli.admin.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/tmp/cache/intelli.admin.lang.en.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/tmp/cache/intelli.config.en.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/bootstrap/js/bootstrap-switch.min.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/admin/login.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/admin/templates/default/img/ico/apple-touch-icon-114-precomposed.png
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/bootstrap/css/fontawesome-iconpicker.min.css
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/bootstrap/css/passfield.css
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/admin/templates/default/css/bootstrap-default.css
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/admin/templates/default/img/ico/apple-touch-icon-144-precomposed.png
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/admin/footer.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/js/jquery/jquery.js
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/admin/templates/default/img/ico/apple-touch-icon-72-precomposed.png
404      GET        9l       31w      277c http://192.168.143.163/192.168.143.163/admin/templates/default/img/subrion-logo-lines.png
200      GET      107l      258w     6083c http://192.168.143.163/panel.txt
200      GET      107l      258w     6083c http://192.168.143.163/panel.html
200      GET      107l      258w     6083c http://192.168.143.163/panel.php
200      GET      107l      258w     6083c http://192.168.143.163/panel.asp
200      GET      107l      258w     6083c http://192.168.143.163/panel.aspx
200      GET      107l      258w     6083c http://192.168.143.163/panel.jsp
404      GET        9l       31w      280c http://exfiltrated.offsec/redirect/exfiltrated.offsec/favicon.ico
404      GET        9l       31w      280c http://exfiltrated.offsec/redirect/exfiltrated.offsec/templates/kickstart/css/iabootstrap.css
404      GET        9l       31w      280c http://exfiltrated.offsec/redirect/exfiltrated.offsec/js/jquery/jquery.js
200      GET       34l       66w     1048c http://exfiltrated.offsec/redirect/
200      GET       34l       66w     1048c http://exfiltrated.offsec/redirect.txt
200      GET       34l       66w     1048c http://exfiltrated.offsec/redirect.html
200      GET       34l       66w     1048c http://exfiltrated.offsec/redirect.php
200      GET       34l       66w     1048c http://exfiltrated.offsec/redirect.asp
200      GET       34l       66w     1048c http://exfiltrated.offsec/redirect.aspx
200      GET       34l       66w     1048c http://exfiltrated.offsec/redirect.jsp
200      GET        8l       16w      142c http://192.168.143.163/robots.txt
200      GET        4l        6w      637c http://192.168.143.163/sitemap.xml
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/tmp/cache/intelli.lang.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/templates/kickstart/img/logo.png
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/js/jquery/jquery.js
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/templates/kickstart/css/iabootstrap.css
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/js/frontend/footer.js
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/tmp/cache/intelli.config.en.js
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.css
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/js/intelli/intelli.minmax.js
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/modules/fancybox/js/jquery.fancybox.pack.js
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/js/bootstrap/js/bootstrap.min.js
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/favicon.ico
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/js/intelli/intelli.js
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/templates/kickstart/css/user-style.css
404      GET        9l       31w      280c http://exfiltrated.offsec/terms/exfiltrated.offsec/templates/kickstart/js/app.js
200      GET      517l      893w    18995c http://exfiltrated.offsec/terms/
200      GET        2l        6w      104c http://exfiltrated.offsec/web.xml
404      GET        9l       31w      280c http://exfiltrated.offsec/Redirect/exfiltrated.offsec/templates/kickstart/css/iabootstrap.css
404      GET        9l       31w      280c http://exfiltrated.offsec/Redirect/exfiltrated.offsec/favicon.ico
404      GET        9l       31w      280c http://exfiltrated.offsec/Redirect/exfiltrated.offsec/js/jquery/jquery.js
200      GET       34l       66w     1048c http://exfiltrated.offsec/Redirect/
200      GET       34l       66w     1048c http://exfiltrated.offsec/Redirect.txt
200      GET       34l       66w     1048c http://exfiltrated.offsec/Redirect.html
200      GET       34l       66w     1048c http://exfiltrated.offsec/Redirect.php
200      GET       34l       66w     1048c http://exfiltrated.offsec/Redirect.asp
200      GET       34l       66w     1048c http://exfiltrated.offsec/Redirect.aspx
200      GET       34l       66w     1048c http://exfiltrated.offsec/Redirect.jsp
200      GET        0l        0w        0c http://exfiltrated.offsec/Actions/
200      GET        0l        0w        0c http://exfiltrated.offsec/Actions.txt
200      GET        0l        0w        0c http://exfiltrated.offsec/Actions.html
200      GET        0l        0w        0c http://exfiltrated.offsec/Actions.php
200      GET        0l        0w        0c http://exfiltrated.offsec/Actions.asp
200      GET        0l        0w        0c http://exfiltrated.offsec/Actions.aspx
200      GET        0l        0w        0c http://exfiltrated.offsec/Actions.jsp
200      GET        1l        1w       53c http://exfiltrated.offsec/Cron/
200      GET        1l        1w       53c http://exfiltrated.offsec/Cron.txt
200      GET        1l        1w       53c http://exfiltrated.offsec/Cron.html
200      GET        1l        1w       53c http://exfiltrated.offsec/Cron.php
200      GET        1l        1w       53c http://exfiltrated.offsec/Cron.asp
200      GET        1l        1w       53c http://exfiltrated.offsec/Cron.aspx
200      GET        1l        1w       53c http://exfiltrated.offsec/Cron.jsp
404      GET        0l        0w        0c http://exfiltrated.offsec/3784.html
200      GET        1l        1w       53c http://exfiltrated.offsec/CRON/
200      GET        1l        1w       53c http://exfiltrated.offsec/CRON.txt
200      GET        1l        1w       53c http://exfiltrated.offsec/CRON.html
200      GET        1l        1w       53c http://exfiltrated.offsec/CRON.php
200      GET        1l        1w       53c http://exfiltrated.offsec/CRON.asp
200      GET        1l        1w       53c http://exfiltrated.offsec/CRON.aspx
200      GET        1l        1w       53c http://exfiltrated.offsec/CRON.jsp
200      GET       13l       31w      473c http://exfiltrated.offsec/hybrid/index.php
200      GET       13l       31w      473c http://exfiltrated.offsec/hybrid/
404      GET        0l        0w        0c http://exfiltrated.offsec/worksheet.txt
404      GET        0l        0w        0c http://exfiltrated.offsec/workathome.html
404      GET        0l        0w        0c http://exfiltrated.offsec/wordGenBio.aspx
404      GET        0l        0w        0c http://exfiltrated.offsec/wmg.jsp

```
### files

```

```
# curl 

```
HTTP/1.1 302 Found
Date: Sun, 08 Jun 2025 08:24:48 GMT
Server: Apache/2.4.41 (Ubuntu)
Set-Cookie: INTELLI_06c8042c3d=8ref60ncrcmboukdqkn806vhrq; path=/
Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: no-store, no-cache, must-revalidate
Pragma: no-cache
Set-Cookie: INTELLI_06c8042c3d=8ref60ncrcmboukdqkn806vhrq; expires=Sun, 08-Jun-2025 08:54:48 GMT; Max-Age=1800; path=/
Location: http://exfiltrated.offsec/
Content-Length: 0
Content-Type: text/html; charset=UTF-8



```
# curl - robots

```
HTTP/1.1 200 OK
Date: Sun, 08 Jun 2025 08:24:48 GMT
Server: Apache/2.4.41 (Ubuntu)
Last-Modified: Thu, 14 Jun 2018 05:04:54 GMT
ETag: "8e-56e930a344980"
Accept-Ranges: bytes
Content-Length: 142
Vary: Accept-Encoding
Content-Type: text/plain

User-agent: *
Disallow: /backup/
Disallow: /cron/?
Disallow: /front/
Disallow: /install/
Disallow: /panel/
Disallow: /tmp/
Disallow: /updates/
```

# enumeration
