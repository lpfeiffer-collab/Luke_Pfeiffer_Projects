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
  
  - [ ] Steps to recreate: You must first have some posting privelages. You will then need to create a new post and give it a title name. You will then need to post any youtube url with the \x3c escaping characters for your xss sxript. 
  `[embed src='http://www.youtube.com/embed/sss\x3csvg onload=alert(1)\x3e'][/embed]`
 
 - [ ] Affected source code:
    - [Link 1](https://wpscan.com/vulnerability/8768)

### 2. (Required) Authenticated elements (XSS)
  - [ ] Summary: By inserting a script into the HTML tags that are not closed a hacker can post his attack by simply having a user point there mouse on HTML text.
    - Vulnerability types:Cross-Site Scripting (XSS)
    - Tested in version:4.2.2
    - Fixed in version: 4.2.5
  
  - [ ] GIF Walkthrough: 
  <img src="https://github.com/lpfeiffer-collab/codepath_homework/blob/WordPress_Pentesting/Vuln%202.gif" width="800">

- [ ] Steps to recreate: You must first have some posting privelages. You will then need to create a new post and give it a title name. You will then need to post this 
  `[caption width="1" caption='<a href="' ">]</a><a href=" onmouseover='alert("xss attack")' ">Click Now</a>`. 
 
 - [ ] Affected source code:
    - [Link 1](http://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/)

### 3. (Required) Authenticated Stored XSS
  - [ ] Summary: This one is similar to the embedded youtube url xss. Using the href html attribute to remain unclosed the injected code will remain unfiltered. Using </a> the injection is closed and stored in the code. 
    - Vulnerability types:Cross-Site Scripting
    - Tested in version:4.2.2
    - Fixed in version: 4.2.3
 
 - [ ] GIF Walkthrough: 
  <img src="https://github.com/lpfeiffer-collab/codepath_homework/blob/WordPress_Pentesting/Vuln%203.gif" width="800">
 
 - [ ] Steps to recreate: You need to create a post containing the following 
  `<a href="[caption code=">]</a><a title=" onclick=alert('xss123') ">Click Now</a>`.
 
 - [ ] Affected source code:
    - [Link 1](https://www.vulnerability-lab.com/resources/documents/531.txt)

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
