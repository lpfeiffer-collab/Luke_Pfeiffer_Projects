# Project 7 - WordPress Pentesting

Time spent: **7** hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. (Required) Authenticated Embedded URL (XSS)
  - [ ] Summary: By using an embedded URL that contains a script an attack can occur when the url is activated. In this case a Youtube URL is used. 
  The HTML sanitization feature which filters out backslashes is unable to filter out "\x3c" and this allows the script to be run. 
    - Vulnerability types:Cross-Site Scripting (XSS)
    - Tested in version:4.2.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: 
  <img src="https://github.com/lpfeiffer-collab/codepath_homework/blob/WordPress_Pentesting/Vuln%201.gif" width="800">
  - [ ] Steps to recreate: You must first have some posting privelages. You will then need to create a new post and give it a title name.
  You will then need to post any youtube url with the \x3c escaping characters for your xss sxript. 
  "[embed src='http://www.youtube.com/embed/sss\x3csvg onload=alert(1)\x3e'][/embed]"
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 2. (Required) 
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 3. (Required) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
