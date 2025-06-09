# nmap 

```
# Nmap 7.95 scan initiated Mon Jun  9 09:17:42 2025 as: /usr/lib/nmap/nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/tcp80/tcp_80_http_nmap.txt -oX /home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/tcp80/xml/tcp_80_http_nmap.xml 192.168.114.110
Nmap scan report for 192.168.114.110
Host is up, received user-set (0.24s latency).
Scanned at 2025-06-09 09:17:42 EDT for 73s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 63 Apache httpd 2.4.52
|_http-malware-host: Host appears to be clean
|_http-referer-checker: Couldn't find any cross-domain scripts.
| http-vhosts: 
|_128 names had status 200
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
|_http-comments-displayer: Couldn't find any comments.
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-methods: 
|_  Supported Methods: HEAD GET POST OPTIONS
|_http-server-header: Apache/2.4.52 (Ubuntu)
|_http-date: Mon, 09 Jun 2025 13:17:54 GMT; -1s from local time.
|_http-feed: Couldn't find any feeds.
| http-php-version: Logo query returned unknown hash 1e792384931ccfb141a8509eb56fde6e
|_Credits query returned unknown hash 1e792384931ccfb141a8509eb56fde6e
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-fetch: Please enter the complete path of the directory to save data in.
| http-headers: 
|   Date: Mon, 09 Jun 2025 13:17:53 GMT
|   Server: Apache/2.4.52 (Ubuntu)
|   Connection: close
|   Content-Type: text/html;charset=UTF-8
|   
|_  (Request type: HEAD)
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-title: Index of /
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-chrono: Request times for /; avg: 555.77ms; min: 550.15ms; max: 559.58ms
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
|_http-errors: Couldn't find any error pages.
|_http-mobileversion-checker: No mobile version detected.
| http-sql-injection: 
|   Possible sqli for queries:
|     http://192.168.114.110:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=N%3BO%3DD%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=D%3BO%3DD%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DD%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DD%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=N%3BO%3DD%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://192.168.114.110:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|_    http://192.168.114.110:80/?C=N%3BO%3DA%27%20OR%20sqlspider
| http-enum: 
|_  /: Root directory w/ listing on 'apache/2.4.52 (ubuntu)'
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
| http-grep: 
|   (1) http://192.168.114.110:80/: 
|     (1) ip: 
|_      + 192.168.114.110
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1
|     /icons/
|       gif: 1
|   Longest directory structure:
|     Depth: 1
|     Dir: /icons/
|   Total files found (by extension):
|_    Other: 1; gif: 1
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
Service Info: Host: 127.0.0.1

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun  9 09:18:55 2025 -- 1 IP address (1 host up) scanned in 72.59 seconds

```

# nikto 

```

- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          192.168.114.110
+ Target Hostname:    192.168.114.110
+ Target Port:        80
+ Start Time:         2025-06-09 09:17:43 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.52 (Ubuntu)
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ /: Directory indexing found.
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ Apache/2.4.52 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.
+ OPTIONS: Allowed HTTP Methods: HEAD, GET, POST, OPTIONS .
+ /./: Directory indexing found.
+ /./: Appending '/./' to a directory allows indexing.
+ //: Directory indexing found.
+ //: Apache on Red Hat Linux release 9 reveals the root directory listing by default if there is no index page.
+ /%2e/: Directory indexing found.
+ /%2e/: Weblogic allows source code or directory listing, upgrade to v6.0 SP1 or higher. See: http://www.securityfocus.com/bid/2513
+ ///: Directory indexing found.
+ /?PageServices: The remote server may allow directory listings through Web Publisher by forcing the server to show all files via 'open directory browsing'. Web Publisher should be disabled. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-1999-0269
+ /?wp-cs-dump: The remote server may allow directory listings through Web Publisher by forcing the server to show all files via 'open directory browsing'. Web Publisher should be disabled. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-1999-0269
+ ///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////: Directory indexing found.
+ ///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////: Abyss 1.03 reveals directory listing when multiple /'s are requested. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1078
+ /.env: .env file found. The .env file may contain credentials.
+ 7730 requests: 0 error(s) and 17 item(s) reported on remote host
+ End Time:           2025-06-09 09:54:31 (GMT-4) (2208 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested

```

# screenshot


# whatweb

```
WhatWeb report for http://192.168.114.110:80
Status    : 200 OK
Title     : Index of /
IP        : 192.168.114.110
Country   : RESERVED, ZZ

Summary   : Apache[2.4.52], HTTPServer[Ubuntu Linux][Apache/2.4.52 (Ubuntu)], Index-Of

Detected Plugins:
[ Apache ]
	The Apache HTTP Server Project is an effort to develop and
	maintain an open-source HTTP server for modern operating
	systems including UNIX and Windows NT. The goal of this
	project is to provide a secure, efficient and extensible
	server that provides HTTP services in sync with the current
	HTTP standards.

	Version      : 2.4.52 (from HTTP Server Header)
	Google Dorks: (3)
	Website     : http://httpd.apache.org/

[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	OS           : Ubuntu Linux
	String       : Apache/2.4.52 (Ubuntu) (from server string)

[ Index-Of ]
	Index of

	Google Dorks: (1)

HTTP Headers:
	HTTP/1.1 200 OK
	Date: Mon, 09 Jun 2025 13:17:43 GMT
	Server: Apache/2.4.52 (Ubuntu)
	Vary: Accept-Encoding
	Content-Encoding: gzip
	Content-Length: 338
	Connection: close
	Content-Type: text/html;charset=UTF-8



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
    target_url: "http://192.168.114.110:80/",
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
    output: "/home/kali/OSCP/Exam/192.168.114.110/results/192.168.114.110/scans/tcp80/tcp_80_http_feroxbuster_dirbuster.txt",
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
MSG      0.000 feroxbuster::heuristics detected directory listing: http://192.168.114.110:80/ (Apache)

```
### files

```

```
# curl 

```
HTTP/1.1 200 OK
Date: Mon, 09 Jun 2025 13:17:42 GMT
Server: Apache/2.4.52 (Ubuntu)
Vary: Accept-Encoding
Content-Length: 557
Content-Type: text/html;charset=UTF-8

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<html>
 <head>
  <title>Index of /</title>
 </head>
 <body>
<h1>Index of /</h1>
  <table>
   <tr><th valign="top"><img src="/icons/blank.gif" alt="[ICO]"></th><th><a href="?C=N;O=D">Name</a></th><th><a href="?C=M;O=A">Last modified</a></th><th><a href="?C=S;O=A">Size</a></th><th><a href="?C=D;O=A">Description</a></th></tr>
   <tr><th colspan="5"><hr></th></tr>
   <tr><th colspan="5"><hr></th></tr>
</table>
<address>Apache/2.4.52 (Ubuntu) Server at 192.168.114.110 Port 80</address>
</body></html>


```
# curl - robots

```

```

# enumeration
