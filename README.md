# sigintz

# Project 7 - WordPress Pentesting

Time spent: **8** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

0. (Required) -- WordPress page shows version
  - [x] Summary: Page exists which reveals WordPress version is installed.
    - Vulnerability types: A10 Insecure Configuration Management
    - Tested in version: 4.2
    - Fixed in version: Website owner responsibility
  - [x] GIF Walkthrough: /0-insecure-config-mgmt.gif
  - [x] Steps to recreate: add /readme.html to WP domain URL in browser
  - [x] Affected source code: /public/readme.html
    - [Link 0](http://wpdistillery.vm/readme.html)
1. (Required) -- User enumeration
  - [x] Summary: Enumerating users by id may reveal information about users in the system.
    - Vulnerability types: OWASP-AT-002 Testing user enumeration
    - Tested in version: 4.2
    - Fixed in version: 4.3.1
  - [x] GIF Walkthrough: /1-user-enumeration.gif
  - [x] Steps to recreate: Modify URL where id=# to increment and probe record numbers
  - [x] Affected source code:
    - [Link 1](http://wpdistillery.vm/wp-admin.php)
2. (Required) -- Persistent Cross-Site Scripting
  - [x] Summary: An unauthenticated attacker can inject JavaScript in
WordPress comments. The script is triggered when the comment is viewed.
    - Vulnerability types: A7-Cross-Site Scripting (XSS)
    - Tested in version: 4.2
    - Fixed in version: 4.2.2
  - [x] GIF Walkthrough: /2-xss.gif
  - [x] Steps to recreate: See file 2/2.txt
  - [x] Affected source code: public/wp-comments-post.php
    - [Link 2](https://www.exploit-db.com/exploits/36844/)

## Assets

// List any additional assets, such as scripts or files
See folders in repository: 0, 1, 2 with 0.txt, 1.txt and 2.txt

## Resources

- wpvuln.com
- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

// Describe any challenges encountered while doing the work

- Many plugins with documented vulnerabilities were paid or difficult to access
- MacBook Air machine with 1.1 Ghz and 8 GB memory was slow to run VM and all processes

## License

    Copyright [2018] SIGINT Z

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
