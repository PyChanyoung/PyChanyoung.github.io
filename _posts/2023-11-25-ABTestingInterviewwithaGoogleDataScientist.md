---
layout: single
title: "A/B Testing Interview with a Google Data Scientist"
categories: Interview
tag: [Data Engineer, Interview]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

**Note**: The following content is summarized from [A/B Testing Interview with a Google Data Scientist](https://youtu.be/2sWVLMVQsu0) from the [Jay Feng](https://www.youtube.com/@iqjayfeng) channel.

```
Question

Let's say you designed an experiment to measure the impact financial rewards have on users' response rates.

The result shos that the treatment group with $10 rewards has a 30% response rate, while the control group without rewards has a 50% response rate.
```

The problem says that the group with a little reward has a higher response rate than the group with no pay. This is very strange if we think in a normal way. It might mean we missed something in the experiment. In the start of the interview, we can ask many questions. We can ask about how the experiment was made, what the reward is like, and what the people who joined are like.

### Script

<details>
  <summary><b>Initial Discussion on Experiment Results</b></summary>
  <p>
    <strong>Interviewer:</strong> "This is an A/B testing question. Let's say that you design an experiment to measure the impact of financial rewards on users' response rates. So let's say it's a survey and the result shows that the treatment group with $10 in rewards has a 30% response rate, while the control group without rewards has a 50% response rate. This is... You know obviously on and so can you explain what might have happened and how you can improve this experimental design?"
  </p>
  <p>
    <strong>Candidate:</strong> "Yes, for sure. So this definitely seems odd. Because I mean, general intuition says that if you give someone a financial incentive so then they tend to reciprocate or respond more. If the control group itself is having 50% then the treatment group should at least have 50%.<br><br>So some things I would definitely think is, I mean one would be like I would probably trust the experimentation process and then see that okay maybe offering financial incentive is discouraging them. Because they might feel that we are kind of like buying their response and they don't want to really do it. So that could be a hypothesis that seems very unlikely but that could be the reason everything went well and that is what happening and the company is better of just by not giving incentives.<br><br>Another thing could be something in terms of sample ratio mismatch. You know like for whatever reason the randomization is not really happening. So let's say if we plan to do like 50/50 treatment and control group, so that randomization or that division is not really happening. So, we can go and check on that for example, let's say that the link to the survey is systematically getting broken for people in the reward group maybe we are attaching the reward link where they can go and claim and because of that the load time is increasing and they are getting frustrated.<br><br>So basically the experience of filling this survey, might be systematically bad for people in the reward group. So that is a plausible reason to happen and this generally happens more often than not in companies so, when they are trying to render like a new feature and it is taking systematically longer than expected and people get frustrated and they don't continue with the process flow, something like that could be happening.<br><br>So I would definitely go and test if everything is same in terms of time taken to complete among the people who converted what is the time taken to complete that survey form for control and treatment and see if they're significantly different. So that is something I would definitely test.<br><br>So let's say if even that checks out there is no problem in terms of like how the survey is loading, in terms of you know even the survey completion times it's pretty much the same, not significant difference, then in order to again I would probably go back to my initial hypothesis saying that for whatever reason people are feeling that giving them reward is kind of like buying their loyalty and not really liking it and they're less likely to complete the survey, so in order to again reinforce this hypothesis I would test something like create like one more group with something in between like a $5 reward and $6 reward, and see like how the conversion rate is.<br><br>So based on this high post hypothesis let's say if I give like a $5 reward, then the conversion rate should be around like between 30% and 50%. If that is again happening then reinforces my hypothesis and then I conclude that it is probably better not to give a reward. So I will create like an interim group something in between or something more than $10 and see if it is around still 30% or even reduced. So I will do something like that like at least from my research work I seen multiple papers that use financial rewards to improve survey rates. So I don't believe that is the case and I would probably go back and check my experiment how my experiment is getting connected again and see if I can fix anything there."
  </p>
</details>

<details>
  <summary><b>Exploring Experiment Design Improvements</b></summary>
  <p>
    <strong>Inteviewer:</strong> "Gotcha. What could be an alternative explanation that is there any worth towards increasing the size of the reward in this case like maybe people think $10 is too small, would be then worth testing or is it the fact that maybe the control group without any kind of reward gives them some sort of other benefit towards like the $10?"
  </p>
  <p>
    <strong>Candidate:</strong> "So, if this experiment was really testing the impact of reward on survey completion rates, then even the call to action or the message should be exactly identical except the fact or like an email saying that 'Hey, if you complete this survey, then you will get this you can claim the strength reward.'. If whatever reason control group had some other incentive so maybe what I am testing is not the effectiveness of $10 reward compared to the control I am testing the effectiveness of $10 reward compared to the incentive in control I will definitely go back and look at the exact call to action that I am sending my customers or target population and then see whether there is this I mean what I'm testing is what I'm trying to test."
  </p>
</details>

<details>
  <summary><b>Testing Different Reward Strategies</b></summary>
  <p>
    <strong>Interviewer:</strong> "Gotcha. So, for an example what if you advertise it in the subject line like $10 reward for the treatment group but then for the control group you can't really say $10 reward at all, then you have to completely change the subject line in that case, right? So is that testing multiple variants then or is that testing multiple effects or is that still like a valid test?"
  </p>
  <p>
    <strong>Candidate:</strong> "So, for the same reward you can always give the call to action in multiple ways for example so there is some research that says that so for the same $10 reward if you give store credit versus like a free cash or you know like an amazon gift card, so the effects are slightly different.<br><br>Reward might be the same, but the way you operationalize it will have different effects. In the same way like having an email with subject line that says $10 reward seems kind of like spam. Because you get all these spam emails that look like too good to be true and people are now used to them and you used to just archiving them or deleting them or reporting a spam.<br><br>So maybe you're not operationalizing in a good manner, so you could test like a different call to action where subject line is similar to the control group but it's just the reward that when they open the email that is prompting them to complete it.<br><br>So, if for the same $10 reward having it in the subject versus just having it in body definitely will have different effects. Again, so the reason why we would be testing them is to see what's working and use it for the entire population of users.<br><br>So, you test it on a sample and then use it for the entire population. There is a downstream process that will use the results of this experiment so you would want to design in such a way, that can be used in the downstream for the population of users.<br><br>So I would test both the cases and then see what's exactly happening."
  </p>
</details>

<details>
  <summary><b>Final Thoughts and Future Directions</b></summary>
  <p>
    <strong>Interviewer:</strong> "Yeah, I agree with that too specifically I was thinking that if one email is more catered towards helping out because you should help out on our survey versus another one is more catered towrads here's $10 and it's pretty easy way to make $10 then you're kind of biasing for people that have a financial incentive versus people that just have a regular kind of helping out incentive towards your research study. So that makes sense. Let's say that this is a corrupt result saw changes in a variety of places right whether it's the subject line or something else and let's say you want to run like a great experiment next time. You still have some financial budget. You mentioned that you would just test $5 next to see what would happen is that the perfect experiment that you could run next time like what is the perfect experiment that you would run instead of this like $10 kind of financial reward system? Could you just like describe it from start to end?"
  </p>
  <p>
    <strong>Candidate:</strong> "Oh yeah, sure. So the goal that we are trying to optimize here, is conversion rates. I mean, we want as many people to fill the survey as possible. So, it's not just the completion rate we would want them to put effort into filling the survey. So we would look at the completeness of the survey or the length of if there are text questions we look at the length of the text all that. So, even those should also be considered as the winning I mean the important metrics not just the conversion rate.<br><br>So I will first decide on what are is important to me so are those like the coimpleteness is that important as well, so if it is what is the weight rate so I will create like a hybrid metric which is representative of what success looks like for me. So that will be my step one is to have like a good overall metric.<br><br>So once that is done, I've decided that I want to maximize this new metric that I created. I want that to be higher for my winning group and which I would subsequently implement for everyone else. So the way that I would decide on sample size for this experiment or the amount of time that this should run, so that will be based on practical significance. Because like given infinite sample size you can detect any smallest of the effects. So it doesn't make sense to just put tens of thousands of people because just to detect an effect.<br><br>I will see what the practical significant for me is. So if you take this example of conversion rate, so does 5% increase in conversion rate makes sense for me to implement this reward. If yes, anything less probably doesn't make sense 5% or more is the only one that I would be interested in. So then I will get my sample size based on that effect size 5% imporvement given distributions of that metric I will get the sample size from.<br><br>So you have like let's say 80 power and 0.05 practical significance and the effect size any sample size calculator will give me like what the sample size for each group should be and I will see if that makes sense for me. So if I have more users that means I can test more groups, so that's how I will decide my samples so I will always decide my sample size based on practical significance. I'm not saying that okay like these are the people that we used for something else I will just test it.<br><br>So we'll always take that as the starting point. So the next step after I decide on sample size would be to see again, you know to test different variants like this case. So okay, we've already seen this so there is a drop because of reward, so then now I can just have my control group without incentive then I have my other treatment gorup with $10 reward, if I know that everything else checks out which is you know there is no sample ration mismatch everything was working well and I just want to test this hypothesis again you know like subject line versus some other reward so I will test some rewards something in between which is like $5 reward if that is enough so this is kind of like a pricing question like what is the optimal price or incentive for you to like finally set, so I will test something like a $5 reward and I will also test without subject line having that as just a push inside the email to send.<br><br>So I will not really test the same exact $10 reward in the subject line for 30% conversion rate, becuase I already know that. So if my $5 reward falls somewhere between then I know that people are getting discouraged by being shown this financial incentive in the subject line itself. So if I don't see that then I have like new problems but otherwise like I don't have to test this group again. Because now I am assuming that everything worked as is. So I will only test the other one and definitely I will test the other one without having this $10 reward in the subject."
  </p>
</details>

<details>
  <summary><b>Last Question and Discussion</b></summary>
  <p>
    <strong>Interviewer:</strong> "Gotcha. Cool. Last question, this one is kind of tangentially related but let's say that we ran this new experiment again with like the money $10 reward we made everything correct, now we see that the financial incentive has increased the response rate let's say the 60% versus the regular one is 50%. But we have a feeling that after looking through a few of them that the responses are you know like too fast like the sentences are like they're like very short you know they're actually not doing a lot of feedback. What would you think is happening there you know kind of obviously maybe they're just based on the financial success but like what would you do going forward after like seeing this?"
  </p>
  <p>
    <strong>Candidate:</strong> "Yeah, so I think I kind of touched upon this in the previous one where so I said I'll create like a hybrid metric which takes care of not just the conversion rate but also the number of complete responses and all the other things which is like the length of the text, so all this switch matters to me so that's why if you see like a lot of companies so they don't just have like conversion rate as they like single metric they have like multiple metrics as a combination of these metrics with weights as their metric that they're optimizing for I mean even like tech companies you know like conversion rate itself is not the main thing like you know the total revenue or daily active users amount of time they're spending amount of people there, amount of activity they are doing. So there is like a holistic metric that will be used for optimization. So that will be the outcome metric of the experiment.
  <p>
    <strong>Interviewer:</strong> "Yeah that makes sense. And being able to calculate that is better towards an overall improvement there. So cool."
  </p>
</details>

<style>
details summary {
  cursor: pointer;
  padding: 10px;
  font-size: 18px; /* 글꼴 크기를 더 크게 조정 */
  color: #FFFFFF; /* 밝은 색상으로 변경 */
}

details p {
  padding: 5px;
  font-size: 12px; /* 텍스트 글꼴 크기 조정 */
  color: #CCCCCC; /* 밝은 회색으로 텍스트 색상 변경 */
}

details p strong {
  font-weight: bold;
  color: #FFFFFF; /* 강조 텍스트 색상도 밝게 조정 */
}
</style>
