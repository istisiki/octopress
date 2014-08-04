--- 
layout: post
status: publish
published: true
title: Couldn't Load Plugin - Chrome Flash Plugin Error on Linux
author: stacey
author_login: stacey
wordpress_id: 1821
wordpress_url: http://blog.staceycardoso.com/?p=1821
date: 2013-02-03 09:06:24 +08:00
categories: 
- debugging
tags: []

comments: []

---
<strong>Setup</strong>
OS: Ubuntu 12.10
Chrome: v23.0.1271.97

<strong>Solutions</strong>
<ul>
	<li>Remove the problematic component.
[code]
rm -r ~/.config/google-chrome/PepperFlash
# OR
chmod 000 $HOME/.config/google-chrome/PepperFlash/11.5.31.138/
[/code]

Solution from <a href="https://productforums.google.com/forum/#!msg/chrome/PEgELQH5zcg/c5lHKwslBcwJ" target="_blank">Sle_Deen</a> and <a href="https://code.google.com/p/chromium/issues/detail?id=173790#c5" target="_blank">commenter #5</a>.</li>
	<li>Alternative Solution
Use HTML5. Just add "&amp;html5=True" to the end of your video URL. Know more about Youtube+HTML5 <a href="http://www.youtube.com/html5" target="_blank">here</a>.</li>
</ul>

You can follow the progress of the permanent fix <a href="https://code.google.com/p/chromium/issues/detail?id=173790#c5" target="_blank">here</a>.
