--- 
layout: post
status: publish
published: true
title: Pretty Pretty Code
author: stacey
author_login: stacey
wordpress_id: 2228
wordpress_url: http://blog.staceycardoso.com/?p=2228
date: 2013-07-23 21:42:38 +08:00
categories: 
- coding
- coding pet peeve
tags: []

comments: []

---
[caption id="attachment_2211" align="aligncenter" width="451"]<a href="http://xkcd.com/1144/"><img class="size-full wp-image-2211" title="&lt;A&gt;: Like &lt;/a&gt;this. " alt="XKCD: Tags" src="http://blog.staceycardoso.com/wp-content/uploads/2013/07/tags-1.png" width="451" height="57" /></a> XKCD: Tags[/caption]

Or you can NOT follow their indentation rules.
<span style="color: #808080;">(For the purpose of this exercise, this function has a long parameter list but this shouldn't exist in real life else, <a href="http://www.cleancoders.com/" target="_blank">Uncle Bob</a> will haunt you in your sleep.)</span>

[code language="ruby"]
# reader / i have a very wide screen
function_foo(the, quick, brown, fox, jumps, over, the, lazy, dog)

# OCD reader
function_foo(the, quick, brown, fox,
             jumps, over, the, lazy,
             dog)

# short fuse reader
function_foo(the, quick, brown,
  fox, jumps, over, the, lazy,
  dog)

# neurotic
function_foo(
  the,
  quick,
  brown,
  fox,
  jumps,
  over,
  the,
  lazy,
  dog)

# neurotic OCD / ohhh... pretty lines
function_foo(the,
             quick,
             brown,
             fox,
             jumps,
             over,
             the,
             lazy,
             dog)

# taking it too far
function_foo
(
  the,
  quick,
  brown,
  fox,
  jumps,
  over,
  the,
  lazy,
  dog
)
[/code]
<p class="clean">I used to spend so many hours just changing the way the variables were indented on a class that I had to change a few lines of. That was back in the day when I still didn't know about 'git blame' / 'svn blame' so I can pass on the blame for the fugly code to someone else.</p>
On my first programming exercises in high school<span style="color: #808080;"> (and even until college)</span>, I employed the <em>'reader'</em> style. I was very unperturbed by the constant horizontal scrolling. <span style="color: #808080;">(I also had very good memory, resorting to single letter variable names that I somehow still remembered how to use 500 LOCs later! Oh, yes. About that. My functions also spanned hundreds of LOCs. What a noob.)</span>

A little after college, I was subjected to my first code review. My <a href="https://www.facebook.com/joanrey.sedigo/" target="_blank">Jedi Master then</a> asked if I read a lot of books because it showed in my code. He then introduced me to the<em> 'neurotic OCD'</em>/<em>'ohhh... pretty lines'</em> style <span style="color: #808080;">(please read in</span> <a href="http://www.youtube.com/watch?v=51zk8BwwF8M" target="_blank">Oleg's voice</a><span style="color: #808080;">)</span>. Some time later, I would develop this perverse need to always have my brackets and parentheses aligned. Hence <em>'taking it too far'</em> was born.

I've since reverted back to the <em>'ohhh... pretty lines'</em> style but I'm also trying this thing called not letting your line be longer than 80 characters. If you have something like this...

[code language="ruby"]
MartialArts::JeetKuneDo::MyNameIsBruceLee.and_i_can_be(:like =&gt; [ 'water',
                                                                  'dragon',
                                                                  'the_wind' ])
[/code]

...you'd still go beyond the 80-character limit. So sometimes I use the <em>'neurotic'</em> style much to the disapproval of <a href="http://dindeelion.wordpress.com/" target="_blank">Odina</a>. She suggested I do this instead.

[code language="ruby"]
# ohhh pretty lines hacked
bruce = MartialArts::JeetKuneDo::MyNameIsBruceLee
bruce.and_i_can_be(:like =&gt; ['water', 'dragon', 'the wind'])
[/code]

So I for me, it's <em>'ohhh... pretty lines'</em> and <em>'neurotic'</em> <span style="color: #808080;">(but only if Odina's hack won't help)</span>.

When I asked my friends what their religions were<span style="color: #808080;"> (</span><a href="http://dindeelion.wordpress.com/" target="_blank">Odina</a><span style="color: #808080;">: 'ohhh... pretty lines';</span> <a href="http://fredbaa.com/" target="_blank">Fred</a><span style="color: #808080;">: 'OCD reader';</span> <a href="http://www.scriptchaos.com/" target="_blank">Pam</a><span style="color: #808080;">: 'neurotic')</span>, Odina and Pam got into a heated <span style="color: #808080;">(albeit friendly)</span> argument as to whose code looked prettier.

Well, as long as I don't need to scroll horizontally, the code is pretty enough.
