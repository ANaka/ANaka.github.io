---
title: "Do twitter bots dream of electric twitter sheep?"
layout: post
date: 2019-06-26
image: /assets/images/
headerImage: false
tag:
- twitter
- science
star: true
category: blog
author: naka
description: 
hidden: false
---
A wild twitter bot appeared as I was browsing this morning. I know these are not difficult to find, but I think they're pretty fascinating, albeit also somewhat disturbing. 

![](/assets/images/2019-06-26-do-twitter-bots-dream-of-electric-twitter-sheep/2019-06-26-10-57-45.png)

Out of an abundance of caution, I blurred out the names here, though it won't be hard to find the account if you want to see for yourself.

There are a number of tools on the web that will try to classify a twitter account as being a bot or a human. A twit-Turing test, if you will. I used one at https://botsentinel.com/ which yielded the following. 

![](/assets/images/2019-06-26-do-twitter-bots-dream-of-electric-twitter-sheep/2019-06-26-11-01-07.png)

I'm pretty amazed by how many of this account's followers appear to be fake too. Here's one example

![](/assets/images/2019-06-26-do-twitter-bots-dream-of-electric-twitter-sheep/2019-06-26-11-23-12.png)

This account has tweeted exactly once since it was created, but has >1k followers. 

One of the most noticeably fake things here is the very obviously computer-generated profile text. 

>A Good And Honest Lady From The USA and Internet in Trump , Single and Still Searching and Meet More friends Here Too

This shows up in a bunch of the follower accounts - here are a some more examples from other accounts following @davidhr4_2:

>I am very cordial. Am caring, sincere, trust worthy, romantic, Compassionate, affectionate, Honest, Faithful and Respective.

>am hardworking and honest human being, trying to make new friends

>am jenny i live in alabama texas am 30yrs of age am hard of hearing lost my hear drum when i was a kid.i love been myself

>Am honest,caring,open-minded,easy going and God fearing woman

>Am easy going person

>am good woman

>well I'm Vivian and am 30 year single with no kids and I was born and raised in. San Diego California /hit me up (vivianbutler301@gmail.com)

>Well am single,with no kids and never been married.whiles looking to find a conscious man to build monogamous relationship and also share good & bad together..

>I am unicorn and very honest

>I am easy going and open minded person I am from Lisbon Maine USA🇱🇷🇱🇷

>I'm very tender, affectionate, feminine and graceful lady with a zest.

>I’m a very easy going woman who love to make friends and love to try new things

>i am melissa,like meeting new friends,go to beach with friends,cooking and listen to music

>im singke with one kidLooking fir serious relationship that can lead to mariage if yiu are interested on me you can add me up on hangout…

>make friends with new people and easy going.......not looking for any fucking problem from any fucking body

To me, these look a lot like someone trained an RNN on twitter profile descriptions or something similar and spat a bunch of crap out from that. There are some other similarities between the accounts. The ones that tweet mostly retweet, and the non RT posts tend to be pictures of attractive women or links from external websites. 

A lot of them also do various permutations of 'Thank for you helping me reach N followers!'
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Thank you for helping me reach 100 followers! I literally couldn’t have done it without you.</p>&mdash; Ernie ken (@Ernieken2) <a href="https://twitter.com/Ernieken2/status/1124236289723830277?ref_src=twsrc%5Etfw">May 3, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Thanks for helping me reach 25 followers! Who else do you think should be following me?</p>&mdash; Anabell Santos (@AnabellSantos5) <a href="https://twitter.com/AnabellSantos5/status/1130499592234176512?ref_src=twsrc%5Etfw">May 20, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


or # new profile pic
<blockquote class="twitter-tweet" data-lang="en"><p lang="und" dir="ltr"><a href="https://twitter.com/hashtag/NewProfilePic?src=hash&amp;ref_src=twsrc%5Etfw">#NewProfilePic</a></p>&mdash; Donna Thomas (@DonnaTh99054311) <a href="https://twitter.com/DonnaTh99054311/status/1135049400366116864?ref_src=twsrc%5Etfw">June 2, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="en"><p lang="und" dir="ltr"><a href="https://twitter.com/hashtag/NewProfilePic?src=hash&amp;ref_src=twsrc%5Etfw">#NewProfilePic</a></p>&mdash; Stella Maris (@Simi54342137) <a href="https://twitter.com/Simi54342137/status/1141022096216285186?ref_src=twsrc%5Etfw">June 18, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I'm not sure why I find this so fascinating. I guess it's just wild to imagine that twitter's network has huge subnetworks composed almost entirely of automated accounts. 

I only recently found out that this is an area of intense research focus. See e.g. [this paper on the 'Bursty' and 'Star Wars' botnets](https://arxiv.org/pdf/1709.06740.pdf). Bot detection is an interesting and ever-evolving ML problem. Sometimes, as for the Star wars botnet, they have some giveaways:
![](/assets/images/2019-06-26-do-twitter-bots-dream-of-electric-twitter-sheep/2019-06-26-12-04-22.png)

e.g. they generate location-tagged tweets from randomly generated locations falling within rectangles covering North America and Europe, which leads to some users doing things like tweeting from Alaska, and then tweeting from the middle of the Atlantic Ocean. 
![](/assets/images/2019-06-26-do-twitter-bots-dream-of-electric-twitter-sheep/2019-06-26-12-05-58.png)

How much do bots matter?
[This](www.eecs.qmul.ac.uk/~tysong/files/TWEB19.pdf) is a pretty interesting study on the structure of botnets and how they impact the activity of human networks. Bots apparently upload a ton of the media content that gets onto twitter
![](/assets/images/2019-06-26-do-twitter-bots-dream-of-electric-twitter-sheep/2019-06-26-12-15-21.png)
but bots and humans seem to exhibit very strong homophily in their interactions on twitter - bots mostly talk to bots, and humans mostly talk to humans. 
![](/assets/images/2019-06-26-do-twitter-bots-dream-of-electric-twitter-sheep/2019-06-26-12-24-49.png)

So it's unclear how much influence bots have on human activity. An interesting subject to be sure, I'll have to read up on it some more. 


[1] Echeverria J, Besel C, Zhou S. 2017. Discovery of the Twitter Bursty Botnet. arXiv [csSI].

[2] Gilani Z, Farahbakhsh R, Tyson G, Crowcroft J. 2019. A Large-scale Behavioural Analysis of Bots and Humans on Twitter. ACM Transactions on the Web (TWEB) 13:7.