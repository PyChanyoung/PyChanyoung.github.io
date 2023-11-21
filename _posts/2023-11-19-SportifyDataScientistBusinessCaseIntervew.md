---
layout: single
title: "Spotify Data Scientist Business Case Interview"
categories: Interview
tag: [Data Engineer, Interview]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

**Note**: The following content is summarized from [Spotify Data Scientist Business Case Interview](https://youtu.be/ALSU1nZaxBo) from the [Jay Feng](https://www.youtube.com/@iqjayfeng) channel.

```
Question

A media company makes its money from monthly subscription fees. The company is considering entering the podcast space.

How would you measure the impact on customer lifetime value of such a move?
```

Step 1. Clarifiying questions & assumptions

Before I get started I want to understand a couple of different things. One I guess how what is the current monetization model and are we assuming that this is spotify and I can kind of make those assumptions for myself?

- Yes so I'd say you could probably choose spotify like the New York Times any sort of media org(organization) that you know primarily does one thing such as let's say blog posts maybe it's even music subscription with spotify's case and then is now thinking about branching into podcasting. And whether that's their own potcast or just featuring spot potcasts. So pretty open here but yeah spotify would be specifically a use case where I believe they'd be kind of entering the podcast space in terms of buying podcasts and then just featuring them on their play. Whereas the New York Times I think is a little bit more so like they're starting podcasts to then kind of sell to their existing member base and subscribers.

I see for example should we assume that like basically spotify let's I'll assume let's say that spotify is like is looking to launch a podcast specific section within their app they're thinking about how to do that and what the impact value will be.

- Yeah I think that's a good assumption.

So, do we want to make a distinction right now about is a are we targeting to introduce podcasts to free users or to premium users or do you want to go after all of them?

- Yeah yes What do you think about that because I think that's actually a pretty crutial question. And would love your take because I don't know if that's something that I would nessesarily have a decision.

Okay so I'm trying to take this as really understand first of all I want to understand why spotify or why podcasts make sense to spotify or what the kind of motivations could be behind them looking into this space and wanting to enter it. So I'm just going to break down a couple things that I know about spotify and then maybe we can fill in the gaps there and then from there we can try to understand what the internal and external motivations would be for them trying to enter this new space.

- Sounds good.

So from an internal perspective I think spotify is split up into really free and then premiere. So premium I understand is that they have a couple different plans so I can go into the plan deatils because I remember some of them off the top of my head but really it's like individual, student and then I think they also have like a family offering.

- Yes

So all three of them are monetized in different ways but let's assume just for now that the monthly revenue per user(MRPU) is approximately seven bucks per month($7/Month).
And then for the free offering I remember them having basically limitations on what..there's more features that are available for premium users of course but really the way that they make their money from free users is ad supported content. And I think that I remember for..We can assume this as well but I think the from the past research that I've just generally read about spotify I think 90% of the user base falls into this premium category and then 10% is ad supported content that sound about right?

- I think so. That does seem kind of high 90 are on premium. Let's make that assumption.

Okay if it seems a little high intuitively, I'm happy to kind of adjust it. So let's go with 25% and 75% split.

- Okay

If we kind of make that assumption then so ad supported content of course you're definitely not getting the monthly revenue per user that you're getting with premium. I'm going to assume that it's likely between half maybe five dollars per user on the top end depending on how heavy the consupmtion of content is through the ad supported model so I'm going to assume that MRPU here is about $3.50 to $5.
I'm gonna, because the standard way to measure like I guess SAS, metrics is usually through harpoo I'm going to convert this into a 12 month figure and then we can have a apple samples comparison or we can leave it at monthly for like a monthly user I'm going to actually assume that it's between 36 and 60 dollars for free user per year per user and then for a premium subscriber it's going to be somewhere between around 84 per year.
Cool, so I guess really the challenge I think that spotify is probably having is with keeping people on their premium subscribtion either keeping people in their premium subscription and prevent them from moving into an ad supported model motivations. Let's go into that so there's a couple things one is keep people from churning, and churning kind of breaks down into actually two angles one is the free offering and the other thing is premium. And there's couple ways that they can go on a premium angle they can either leave or downgrade. So the reason I'm trying to do this is really to understand, What incentive spotify has to launch this, so that they can keep the model that they have today or the monetization of the revenue model that they have today set up. And then for free, I'm thinking that likely just again in the context of chruning I want to keep and say that free and the only really other option is leave. Because there isn't one more option that they could take which is actually to upgrade but that's not part of this framework.

- Yeah

So, two is let's actually look at this from the other angle which is upgrades. So we actually want people to go from free to premium. And then 3rd One is engagement and usage. From that angle is of course I think it implies that we want to either encourage usage of free or encourage uses or premium to spend so that people have more incentive to stay within the app and stay within the ecosystem. But four is also to grow. I think the current market today and this is where I'll get into the competitors now and we'll start transitioning to the external motivations is that there's just not that many options available to people today to stream or consume content in that streaming fashion. There's like a couple of major heavy hitters that you have but int the podcast space it really expands even further grow user base. Are there anything that you think I've missed here on the internal side before we move forward to the external side?

- No I think you actually probably hit on every single one of them. And mainly I think this is great because you're kind of going between growth, upsells, continued engagement and then reducment of churn. which is probably everything you need for SAS at this point.

Cool. Now engagement and usage so I'm going to actually break this down into a couple buckets which is I'm going to look at them differently and then grow.
On engagement I'm going to look at really how do we get people to check out new content. And on usage really the biggest metric here is time spent in app. Grow side well really it'sadding new users to the app. So actaully grow exist in two ways. One is increase number of free users and increase the number of paid users and really the other thing is. So around engagement and usage I think there is the high level metric but there's also things that I would consider like time spent by free and actually free and paid. And really actually around churn, so I don't want to miss that as well why would anybody churn in the first place well. It's because they have another source of consuming content. So, not it's time to look at really the competitors.
I'm gonna look at the leave aspect and they can leave to a couple different options. One is Youtube Music, one is Apple service, and the other is really like I think those are the two biggest names right now and then there's like this other category and that other category breaks down into things like stitcher, let's say pocket casts, and you have like the news agencies as well that all have their own native apps. Is this all making sense for now? And then is there anywhere you want me to clarify and go back to this make sense?

- I think specifically we should probably start drawing it in into how podcasts affect the space right because we're still talking about kind of music and their core business model of spotify. And so specifically we start thinking about how potcasts kind of affect these four metrics where do you think the first one kind of stands out of like all four of them?

I think the biggest reason to launch podcasts is to make sure that people stay, people that are in the spotify ecosystem stay within the spotify ecosystem. So it's really increasing like staying power if you want to call it.

- So decreasement of churn and I guess why do you say that one versus like growth and the other one engagement and then I think was it upsells?

Step 2. Metrics to analyze the decision

Step 3. Quantify decision making

Step 4. Value/Risk Matrix

Step 5. Paying for exclusive content
