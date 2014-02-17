--- 
layout: post
status: publish
published: true
title: Recover Lost Git Stash
author: stacey
author_login: stacey
author_email: staceykay.dc@gmail.com
wordpress_id: 1948
wordpress_url: http://blog.staceycardoso.com/?p=1948
date: 2013-05-26 12:15:52 +08:00
categories: 
- debugging
tags: 
- programming tricks
comments: []

---
[code]
# basic
git fsck --no-reflog 

# only the SHA1 codes of the dangling commits
git fsck --no-reflog | awk '/dangling commit/ {print $3}'

# see a visual respresentation all the commits 
#  including the dangling ones
gitk --all $(git fsck --no-reflog | awk '/dangling commit/ {print $3}')

# apply the commit that was lost
git stash apply &lt;stash's SHA1&gt;
[/code]

<a href="http://stackoverflow.com/questions/89332/recover-dropped-stash-in-git" target="_blank">Source</a>
