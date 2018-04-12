# Free Data Manifesto

You may not even know it, but you're up for auction. Every day, companies bid
with each other to get a hold of your data.
The videos you watch, the queries you search, the messages you send to your
loved ones are all data used to sell your "user profile" to the highest bidder.
They, in turn, use this data to serve you with targeted advertisements.

A cynical person might attribute this to pure malevolence or some grand
conspiracy. The truth, however, is much less grandiose. Tracking user data and
serving targeted advertisements is the only real way to make money on the
internet.

## Why the system is broken

And this would all be tolerable if not for the fact that this data is
used to [spy on you](http://www.bbc.com/news/world-us-canada-23123964),
that this data is poorly kept and [often breached](https://www.theguardian.com/technology/2018/apr/08/facebook-to-contact-the-87-million-users-affected-by-data-breach). It would
be tolerable if corporations didn't run [psychology experiments](https://www.theguardian.com/technology/2014/jul/02/facebook-apologises-psychological-experiments-on-users) on you without consent or use big data to [undermine democracy](https://www.theguardian.com/technology/2017/may/07/the-great-british-brexit-robbery-hijacked-democracy) or [kill free speech](http://youtube.wikia.com/wiki/YouTube_Adpocalypse).

In an ideal world, attention grabbing multimedia ads wouldn't waste  [40% of all bandwidth](https://venturebeat.com/2015/07/08/blocking-ads-can-cut-network-traffic-25-to-40-study-shows/) and a news site wouldn't consist
of [79% ads](https://www.theguardian.com/media/2016/mar/16/ad-blocking-advertising-half-of-data-used-articles).

We've set up a system, in which the only way to survive - is to play
dirty. Reporters, content creators, teachers - all are forced to
either use ads or lose money.

Advertisers, in the effort to keep their clients, always play safe.
Any sign of controversy has advertisers [pulling out](https://www.theguardian.com/technology/2017/mar/25/google-youtube-advertising-extremist-content-att-verizon) of the platform. This
reduces the nature of our online discourse to the lowest common
denominator.

## How much is a user worth?

The best metric we can use for user value is the ARPU or Average Revenue Per User. For stockholders of publicly listed tech companies - it's one of the most important metrics. It essentially tells you,
how much money a company makes per month per user. Multiply it by
the number of users and you get the monthly revenue. [Facebook](https://www.statista.com/statistics/430862/facebook-annualized-advertising-arpu/), [Google](https://www.statista.com/statistics/306570/google-annualized-advertising-arpu/) and other tech giants employ world-class experts
to raise their ARPU (Average Revenue Per User) and *still* only top
out at ~$5 per user per month. Scaled to the huge number of users they
have, it sums up to a hefty amount, but the _per user_ revenue is a
very manageable $5

For smaller websites (news portals, blogs, instructional sites), this
falls even more dramatically. We're talking ARPUs in the tenth of a
dollar range on the lower end of the scale.

## Convenience always wins

The ideal scenario would be for the user to pay for each site
individually, so they wouldn't have to use advertisements or track
you. The problem is - this will never happen.

The amount of sites you visit every month is too large and the revenue per user too small. If you were to pay for websites
individually, you'd end up with dozens of $0.01 monthly subscriptions. So, if
convenience is king and paying for sites is inconvenient - how do we solve this?

## The universal subscription for the internet

We solve this by implementing a single subscription for all of the services currently funded by advertisements. You pay a fixed amount of money once a month and this money
is distributed to the sites you visit by the number of times you visit them
and the amount of time you spend on them.

The platform is implemented using private/public key encryption. The basic
principle is outlined below:

Assume two parties exist:
- Alice - the owner of the website
- Bob - The user browsing the website

Alice has a private key P_a and Bob has a private key P_b

Alice downloads the PayForIt library (js, java, swift - depending on platform)
and implements it into her site.

Bob downloads a PayForIt browser extension or a mobile app.

Let's look at an example where Bob visits Alices website.
1. Bob pays a $5 subscription which is stored on a smart contract in a public
blockchain
2. Alices website provides no content, but server the PayForIt.js script with
a content unlock request signed with P_a
3. Bobs browser extension detects the content unlock request and responds with
Bobs public key, verifying that the subscription has been paid.
4. The script _and_ the extension start a periodic communication, measuring the
elapsed time
5. After the user leaves the site, the browser extension and the script notify
that the session has ended.
6. The session length is written in a public blockchain
7. At the end of the month, all sessions lengths are calculated and funds are
distributed to content creators. 
