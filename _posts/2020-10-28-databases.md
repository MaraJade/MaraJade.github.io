---
layout: post
title: "Databases run the world"
categories: [Software]
tags: [programming]
---

Somehow in my databases class I missed the *very* important fact that pretty
much everything uses them. Not sure how, but then I'm not sure how I passed that
class anyway. But I have discovered this fact, and so I've been kinda sorta
learning about them.

My main motivation for learning databases is, as most things at the moment, my
reddit bot. For some reason when I first created it, I thought a single database
table would be fine. It seemed like it should work, so I just did it that way,
as other ways seemed unecessarily complicated. Except they weren't, and aren't.

When you have a database for a bot on a network with thousands of subscribers,
single tables aren't going to cut it. So much duplicated information, such a
waste! So I decided I should go relearn how multi-relational databases worked. I
did actually learn some of that before, but I'd never really had much of a
chance to use it. It turns out they're kinda simple, but also kinda complicated.
But a little bit of figuring, and I have made one!

Once I'd created my table schemas, I had to figure out how to migrate the data
from the single table to multiple tables. That took some work, and a lot of
fiddling with inner joins. I'm still not sure I quite understand how those work,
though. I knew I was getting somewhere when I wrote a query that worked on the
first try! It was a simple one, but hey, progress!

Then I had to rewrite my bot so that it was querying the new database structure
correctly. That was probably the most difficult bit, and really where my lack of
knowledge about joins came in. Some of those queries probably have too many
select statements and not enough joins, but I think they're fairly compact. They
work though, and that's the important bit!

Testing the bot is always a process, especially since I don't actually have any
tests for it, just manual exploration. Lots of test posts on my test subreddits!
The next thing on my TODO list is to set up actual unit/integration testing for
this thing, which will save me dev time later. But it seems to be working now,
so it's time for the most anxiety-inducing part: launch. Currently putting that
off, but I only just finished and pushed my changes. Pushing to production is
pretty scary, and I want to be prepared for the problems I missed. Not to
mention the fact that I have to migrate the production database to the new
schemas first... Oh, that's going to be stressful. And I don't even have to
worry about users yelling at me directly for it being broken! Mostly just...
performance anxiety I guess. I could confirm it's absolutely perfect but that
anxiety would still be there. I don't know if that ever goes away though, even
for senior devs who've pushed to production dozens of times.

But hey, progress! Now to do tests, and then start working those optional
features I've wanted to add from the start.

Thanks for reading, and may the Force be with you!
