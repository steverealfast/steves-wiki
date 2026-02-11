# **ExoHelp Pilot Feedback \- February 10**

[**VIEW RECORDING \- 65 mins (No highlights)**](https://fathom.video/calls/560821416)

[@0:00](https://fathom.video/calls/560821416?timestamp=0.68) \- **Gilbert, Channie (Bottomline Technologies)**

Oh, big stuff for us. Maybe, unless no one else is coming.

[@0:09](https://fathom.video/calls/560821416?timestamp=9.82) \- **Aravind Karthik (Realfast)**

Hi, Channie. Hi, Ashish. Hi, how you doing? I'm good.

[@0:15](https://fathom.video/calls/560821416?timestamp=15.74) \- **Gilbert, Channie (Bottomline Technologies)**

I'm good. How are you guys?

[@0:18](https://fathom.video/calls/560821416?timestamp=18.58) \- **Aravind Karthik (Realfast)**

Good.

[@0:19](https://fathom.video/calls/560821416?timestamp=19.66) \- **Gilbert, Channie (Bottomline Technologies)**

I just got back from a long weekend, so playing a little bit of catch-up. Angela. Hello. Hope you had a good day.

I did. I was, like, in my wounds over my mass disappointment, like everyone else in New England. Oh, I know.

I'm sorry. So embarrassing. It was just an awful, awful Super Bowl. I yeah, no, I'm just... I have friends on the West Coast, and they were just brutal.

[@0:47](https://fathom.video/calls/560821416?timestamp=47.66) \- **Bresciani, Angela (Bottomline Technologies)**

Like, I'm like, don't. Too soon. Don't even say anything. Too soon. It was sad.

[@0:55](https://fathom.video/calls/560821416?timestamp=55.84) \- **Gilbert, Channie (Bottomline Technologies)**

It was sad. But such as it is with a 23\. You know what? I look at the positive. Like, at least we made it to the Super Bowl.

He's young. Exactly. We'll see next year. Yeah, exactly. All right.

[@1:12](https://fathom.video/calls/560821416?timestamp=72.7) \- **Bresciani, Angela (Bottomline Technologies)**

So where is – and honestly, guys, I don't know if we're even having this meeting, to be honest with you, because I know – but they didn't ask me to cancel it.

[@1:25](https://fathom.video/calls/560821416?timestamp=85.46) \- **Aravind Karthik (Realfast)**

I'm so confused. Hey, guys. I'm an article. Oh, okay. Okay. So, yeah. So I know – sorry.

[@1:32](https://fathom.video/calls/560821416?timestamp=92.68) \- **Bresciani, Angela (Bottomline Technologies)**

I was just saying, Karthik, that I know Pallomi's traveling.

[@1:36](https://fathom.video/calls/560821416?timestamp=96.82) \- **Aravind Karthik (Realfast)**

So I didn't know if we were having this meeting or not. Yeah, Pallomi's traveling, and also Allison is out this week.

So it's just us. So, I mean, while we are all here, I just wanted to quickly check in if any of you had any feedback on the impact analysis piece.

So, Sophie, I think you ran a couple of sessions on ExoHealth last week. So So in case you have any feedback on that, I'm all yours.

So, yeah. And I think, Ashish, you had some too, right? Yeah, I did.

[@2:10](https://fathom.video/calls/560821416?timestamp=130.88) \- **Sharma, Aashish (Bottomline Technologies)**

Yeah. So whoever wants to go first, guys.

[@2:13](https://fathom.video/calls/560821416?timestamp=133.86) \- **Smith, Sophie (Bottomline Technologies)**

Yeah, to be honest, I ran mine just before the last call and I've been out for the last couple of days, so I don't have any further feedback from the last meeting.

No worries.

[@2:23](https://fathom.video/calls/560821416?timestamp=143.42) \- **Sharma, Aashish (Bottomline Technologies)**

We'll jump to Ashish then. Yeah, I was out sick late last week, so I spent some time on it this morning.

And, I mean, overall feedback is, I thought it was really, really valuable information that the impact analysis provides. I think what I really liked, like my favorite part of the whole thing is the evidence component where it, so it provides, so it will help, you know, document what the requirement was.

And then when it's presenting it. It's kind of high-level root cause analysis or just a high-level recap of what it understood.

It provides evidence of, you know, here's the impact analysis summary. So one of the tickets was to, you know, redirect the queue to an email of case.

So instead of going to QA, goes to QB. And as part of its evidence, it provided both the queues with the QID.

Are there members under those queues? I think all of that was really valuable information that would require a BA or an admin to go and manually look into it, which all of that is documented in the ticket.

I thought that was super valuable. The only piece of feedback that I had was specifically around the impacted components.

Can you share with Shish? I'm sorry. Yeah, sure.

[@3:56](https://fathom.video/calls/560821416?timestamp=236.1) \- **Bresciani, Angela (Bottomline Technologies)**

Do you mind sharing just so it'll be easier for us to kind of track what you're talking about? think

Yeah, absolutely.

[@4:01](https://fathom.video/calls/560821416?timestamp=241.68) \- **Sharma, Aashish (Bottomline Technologies)**

Sorry, I shouldn't have a streamer earlier. Let me find the ticket I was talking about. This is okay.

[@4:19](https://fathom.video/calls/560821416?timestamp=259.14) \- **Aravind Karthik (Realfast)**

So can you see my screen? Yes. All right. So what I mentioned earlier about, I really like the evidence component.

[@4:27](https://fathom.video/calls/560821416?timestamp=267.16) \- **Sharma, Aashish (Bottomline Technologies)**

So again, it kind of touches. So here's the requirement as it understood it. It kind of, again, gets the specific queue that we're talking about, what the ID is, how it verified it, the fact that there were no members on it.

So that's something that we should do before go live. Again, all of that was super interesting to me. So this ticket is saying, hey, instead of tickets going to QA, I want it to go to QB.

So again, documented all of that, which was really cool. So The only kind of feedback that I had was in the impacted components section, which you can see, again, this request, I purposely wanted to get a use case where the requirements weren't super documented and it would be somehow how the business would send it to us with like, hey, here's what I want to do, right?

So I purposely kind of wanted to use this as an example to see how would EXO help handle it.

And I'm sure that plays into it. But there were a lot of impacted components that were listed, like, you know, 25 other case flows, six other case triggers.

And I think if it could kind of trim it down to be specific to the relevant components, I think that's the only piece of feedback that I would have.

Besides that, all the other information was super valuable. I also really liked the test cases. I thought it did a really good job of

Documenting functional and regression test cases, the only kind of feedback here would be kind of pie in the sky, if possible, like, is there a way to automate the regression test cases?

Because you wouldn't have, you know, a BA or a business tester kind of going in and doing regression testing.

So if there's a way to automate it, that would be super helpful. But those would be my two pieces of feedback.

Okay, a couple questions. Sorry, guys, I was late.

[@6:34](https://fathom.video/calls/560821416?timestamp=394.9) \- **\+19\*\*\*\*\*\*\*03**

When you said it listed a lot of impacted components, how do you define what is relevant? Like, what is your definition of relevant?

Because it's listing those components that, you know, will have some interaction with the request. I'm just trying to understand how to filter, if you can filter.

Good question.

[@7:03](https://fathom.video/calls/560821416?timestamp=423.1) \- **Sharma, Aashish (Bottomline Technologies)**

Let me see if I can. So I'm guessing it, again, it all kind of comes back to the requirements in the ticket.

So in this example where the requirements were kind of well-listed out, here's the business requirement, here's the scope, here's the goal, here's an example, like it does a good job of identifying the specific components relevant to that requirement.

I think when the requirements are a bit looser in terms of businesses just said, you know, hey, I want to redirect from QA to QB, where a lot of information isn't provided, that's where I'm guessing it's pulling in additional components.

Like, for example, you know, this was a request on cases, but it was pulling in B1 case SLA, EMEA case SLA as triggers.

So I don't know if I'm doing a good job of answering your question, but that's just kind of my thoughts around how it's identifying relevant components.

And I think it kind of comes down to how well the requirements are documented in the ticket. Yeah, no, I get that.

[@8:23](https://fathom.video/calls/560821416?timestamp=503.541) \- **\+19\*\*\*\*\*\*\*03**

mean, the vaguer it is, the wider the net is for the potential impact. So I'm just trying to think through how we could change that.

Now, the only way we can change, in my mind, the only way we can change that is to make the requirement a much more tighter requirement, which is like the original plan where we would have the business, work through XOHelp, what we're now calling XOHelp Pro, which is asking more specific questions, but that took time.

So we You know, if the business actually, and then maybe, you know, if the business was directly interacting with the EXO help, the faster version that we have for you, maybe it would have been a much more specific requirement.

So I think what I'm hearing is if the requirement is tighter, the impact analysis is tighter, I think that is a direct correlation.

So I don't know what else, I guess what I'm saying is I don't know how else we could change that without changing some sort of process in how we gather requirements too.

Or, as the requirements get refined as a BA, if you can refine them further and we can rerun the impact analysis, maybe that helps you kind of get less information presented to you.

It's like, oh, now I, you know, based on everything I'm writing now, rerun this or something along those lines.

So we'll continue to refine that a little bit more. Based on what you're saying, but there's a catch 22 there, where we can't give you less, because if gave you less, it would not be comprehensive, but if it's big, then we're going to give you a lot more, and then you kind of have to refine it further.

So, I get it.

[@10:21](https://fathom.video/calls/560821416?timestamp=621.801) \- **Gilbert, Channie (Bottomline Technologies)**

Well, before we make any changes like that, can I just ask a team, have we taken any of these end to end through the process?

Meaning, you're not doing anything to it, other than putting it into ExoHealth, other than creating a ticket with the details.

Have we taken it all the way through to user testing and gone through one of these to make sure that they're correct, and any feedback from like a developer, or as we're going through test cases, like do they make sense?

Like where we have really specific feedback on this did or did not, this was or wasn't correct, or this did or did not make sense for this ticket?

Have we? Have that yet? I know we've asked Vachelle to look at a few. Yeah, I mean, I'm just saying, if we think these are good, we should be putting these into tickets and letting the team take them and getting the team's feedback, right?

Yeah, for sure. Without a lot of, I don't know that we need, you know, I'd rather not give them a lot of interaction and give them a really great ticket because it has all these details in it and then see what they say.

Like, is this correct? Is this the right level of detail? From our team's build perspective and then going back to our users, can we use these test cases and just stamp it back in a ticket and have them do it?

Those kind of things. I'd really like to get that level of all the way end to end. I think that's a fabulous idea.

That would be great.

[@11:49](https://fathom.video/calls/560821416?timestamp=709.981) \- **\+19\*\*\*\*\*\*\*03**

I haven't done that yet, but we could do it. Yeah, sorry. Go ahead. No, please go ahead.

[@11:58](https://fathom.video/calls/560821416?timestamp=718.241) \- **Sharma, Aashish (Bottomline Technologies)**

I was just saying, just quick update. on other conversation we had with Vishal.

[@12:02](https://fathom.video/calls/560821416?timestamp=722.901) \- **\+19\*\*\*\*\*\*\*03**

We actually connected with Vishal yesterday. Okay, good. And a couple of tickets that Sophie sent over, I think it was Sophie's ticket.

Yes. And he won it. So he hadn't had the chance to look at them, but we walked him through the kind of the structure of the ticket and what we were, what the whole goal of XO Help was, to give him like a background on it.

So he was going to take a look at them, and we are going to reconnect with him on Thursday, right, Karthik?

We have that scheduled? Oh, that's right.

[@12:39](https://fathom.video/calls/560821416?timestamp=759.041) \- **Aravind Karthik (Realfast)**

And we are catching up with him this day before our call. Yep. Yeah.

[@12:45](https://fathom.video/calls/560821416?timestamp=765.761) \- **\+19\*\*\*\*\*\*\*03**

So hopefully, you know, that'll help kind of with that collection. Because, Shani, I wholeheartedly agree with where you're going with this.

We, too, want to make sure, like, it's helping the architecture. And the developers kind of going forward, because that's kind of the goal of the whole process.

[@13:07](https://fathom.video/calls/560821416?timestamp=787.221) \- **Gilbert, Channie (Bottomline Technologies)**

Yeah, I wasn't sure if we were there, because I know I haven't been, you know, participating as much as I wanted to.

But yeah, if we're ready to do that, I think we should be doing that. So I think, you know, from a BA perspective, I would say, let's start using this.

If we think we're ready, let's start using this the way we think we're going to be using it and go all the way through the process.

[@13:29](https://fathom.video/calls/560821416?timestamp=809.101) \- **Bresciani, Angela (Bottomline Technologies)**

Should we wait, Palomi, until Vishal looks at those two tickets from Sophie before we send them any more? No, I don't think so.

[@13:39](https://fathom.video/calls/560821416?timestamp=819.241) \- **\+19\*\*\*\*\*\*\*03**

I think I agree with Shani. Like, let's just, if you guys can, because I haven't heard anything else that we can, we want, I mean, the only thing I've heard is if the content is a lot, but no one's really been able to articulate what we take off of that content.

So now at this point, I'm like, let's just, more, more. It's better, because it's always easier to delete than add.

I would encourage you guys to start using it in your workflow. Okay.

[@14:11](https://fathom.video/calls/560821416?timestamp=851.062) \- **Gilbert, Channie (Bottomline Technologies)**

100%. Because that's the real true test, right? Like, if this is supposed to speed things up, right? It's supposed to give us better detail, better instructions, make things faster, and, you know, less troubleshooting after the fact kind of stuff, right?

Like, let's do it. Let's take the details. If it's epic worthy, spin up the epic, put the right details from all of this stuff into the right parts of the ticket.

**ACTION ITEM: Send ExoHelp tickets to Vishal for review \- [WATCH](https://fathom.video/calls/560821416?timestamp=872.9999)**

**ACTION ITEM: Send ExoHelp tickets to Vishal for review \- [WATCH](https://fathom.video/calls/560821416?timestamp=872.9999)**

And I would say let's get some real feedback on what actually happened end to end. Yeah. So, Sophie, I know you provided a couple.

[@14:43](https://fathom.video/calls/560821416?timestamp=883.862) \- **Bresciani, Angela (Bottomline Technologies)**

So, Joe and Ashish, if you could do the same and send them, you know, to Vishal for just review, that would be great.

Got it.

[@14:54](https://fathom.video/calls/560821416?timestamp=894.142) \- **Vaillincourt, Joe (Bottomline Technologies)**

Are we having all of these go through, Vishal, first?

[@14:57](https://fathom.video/calls/560821416?timestamp=897.762) \- **Gilbert, Channie (Bottomline Technologies)**

Before we... Like, if this is... What's the simpler one? Are we still having Vishal review? Okay. just don't know.

I mean, his bandwidth, he's usually really, really difficult to get. And I think I'm concerned, Angela, about having to try to send him every ticket for review.

Yeah.

[@15:16](https://fathom.video/calls/560821416?timestamp=916.782) \- **Bresciani, Angela (Bottomline Technologies)**

But don't they look at tickets and solutioning anyways? Like, isn't that part of the normal process? And I know this is like a different lens, obviously.

Yeah.

[@15:28](https://fathom.video/calls/560821416?timestamp=928.002) \- **Gilbert, Channie (Bottomline Technologies)**

If it doesn't require solutioning, then no. If it's not a ticket that goes through the Wednesday meeting, then no, right?

They just go straight into a developer or straight into admin to work. So, the tickets that we review, the small portion of tickets that we review on those Wednesday calls are the only ones that are going through solutioning.

Yeah. I mean, I'll to else is straight to the team. Yeah.

[@15:48](https://fathom.video/calls/560821416?timestamp=948.122) \- **Bresciani, Angela (Bottomline Technologies)**

I'll defer to the team whether we want non, I don't know what we call them, non-solutioning tickets to go because it is a new technology, like, I don't know.

I don't know what the right answer is. Because I get the bandwidth issue, too.

[@16:01](https://fathom.video/calls/560821416?timestamp=961.422) \- **Gilbert, Channie (Bottomline Technologies)**

have a different, you know, like, I would say, like, what's the next, if that's not our next step, like, what's the right next step to take?

[@16:07](https://fathom.video/calls/560821416?timestamp=967.902) \- **\+19\*\*\*\*\*\*\*03**

Well, I would ask the question, okay, it sounds like what, based on what Shami said, if, let's say we take Ashish's ticket example, it, it, he would have done the analysis that XOHELP and Impact Analysis would have done, and it's simple enough that my assumption is, he would have deemed it worthy to go straight to the developer, rather than going through the architect to review it and say, yeah, that's the solution, right?

So, is that a correct understanding of your process? Yes. Yep.

[@16:41](https://fathom.video/calls/560821416?timestamp=1001.46) \- **Sharma, Aashish (Bottomline Technologies)**

Yep. Okay.

[@16:42](https://fathom.video/calls/560821416?timestamp=1002.5) \- **\+19\*\*\*\*\*\*\*03**

So then, I think nothing really changes if it's deemed clear enough, and Ashish would have sent it over to a developer anyways.

And if he deems what impact on XOHELP is provided is clear enough, then it would go to the developer anyways, right?

Mm-hmm. It just saved Ashish. Yeah. I would just encourage Aashish to do with due diligence, make sure that you're comfortable with everything that's come out of that.

[@17:11](https://fathom.video/calls/560821416?timestamp=1031.66) \- **Sharma, Aashish (Bottomline Technologies)**

Yeah, I would agree with that. think, you know, as a kind of between, you know, Joe, Sophie, and I, as we're kind of reviewing these tickets, making sure that it has all the information that we know we would pass on to a developer.

And if it does, and the technical solution isn't super complex, we can take it directly to a developer or admin.

However, if it is a, you know, complex enhancement that requires code or flow changes, that is something that we wouldn't actually really take to a, to our architect review, then I think we just kind of follow the same process.

Makes sense.

[@17:59](https://fathom.video/calls/560821416?timestamp=1079.14) \- **Bresciani, Angela (Bottomline Technologies)**

Yeah. Yeah. But to, I. think, Channie, to your point, I get, you know, Vishal's bandwidth, but we need to run enough through Vishal to make sure that, you know, the technical aspect of this or the technical solutioning is working, right?

So, happy medium, I guess. Like, we have to make sure that we feel comfortable or Vishal and Andy feel comfortable that, you know, these solutions are not breaking anything and this is working as expected.

[@18:28](https://fathom.video/calls/560821416?timestamp=1108.58) \- **\+19\*\*\*\*\*\*\*03**

The devs have a good skill set, too, Angela.

[@18:31](https://fathom.video/calls/560821416?timestamp=1111.04) \- **Gilbert, Channie (Bottomline Technologies)**

So, that's, that's part of where I'm thinking is if this is going to a developer, I think a lot of times, and, and so, Jo, she's like, punch me back if I'm wrong, but I feel like a lot of times they, we've actually even started saying we want to give them more solutioning work, right?

Absolutely. An offload, right, Andy and Vishal. I feel like if there's something glaringly obvious, I'm pretty sure they're not going to put it in, and if they do put it in, it's going to be in our UAT environment and we're going to catch it anyway.

Amen.

[@19:00](https://fathom.video/calls/560821416?timestamp=1140.9) \- **Smith, Sophie (Bottomline Technologies)**

Yeah, was wondering whether, just because like you say, Vishal is like, you know, he's already got plenty of tickets to work through as it is.

And sometimes when I chat with him about a ticket, he mentions Nikita quite often as somebody that can maybe look at doing the solution to kind of help him out.

**ACTION ITEM: Add ExoHelp to Feb 12 team call; introduce Nikita as solutioning partner \- [WATCH](https://fathom.video/calls/560821416?timestamp=1167.9999)**

So if we can pull even her in, in addition to Vishal, that might, that might help things. Perfect. I don't want to put it on Nikita.

I know we've got Shavendra and Deep as well, but maybe as a starting point, we could use Nikita and see how that goes.

Right. And we can bring this up on a team call too.

[@19:38](https://fathom.video/calls/560821416?timestamp=1178.52) \- **Gilbert, Channie (Bottomline Technologies)**

I know we've got the full team call on the 12th, so we can let them know like, hey, we're doing this, it's going to look a little different, right, than what you've seen us give you before.

You know, here's what to be, understand how this is being created and, and let us know your feedback, you know, and how, how it's intaking for you.

So I think that's a good thing, Angela, we can talk about on that. Call them Thursday? Yeah.

[@20:01](https://fathom.video/calls/560821416?timestamp=1201.76) \- **Bresciani, Angela (Bottomline Technologies)**

And then we can definitely fold them into this meeting, you know, when needed, just to provide feedback. You you guys can hear directly from them, Pallomi and Karthik.

Awesome. Yeah. So we just need to find more tickets to push through to them, so we can have some good feedback.

Yeah.

[@20:21](https://fathom.video/calls/560821416?timestamp=1221.98) \- **\+19\*\*\*\*\*\*\*03**

And I guess my question is, you know, as you guys progress, we should just continue to talk about the 2B process.

Um, and what that could look like, um, and, and whether there's a situation where you don't pick and choose your tickets and you start running all of your tickets through this process.

Um, at what point do we make those decisions? And what do you need from us to be able to help get there?

Mm-hmm. And I'm, maybe I'm being greedy, but that's kind of how I'm thinking about it. Yeah.

[@20:53](https://fathom.video/calls/560821416?timestamp=1253.34) \- **Bresciani, Angela (Bottomline Technologies)**

I, at least from my end, the biggest challenge we're facing right now is getting time from the business. Um, so, you

We've asked Johnny, we've asked Matt, Tyler, Steph, but it's not a priority for them, so it's really hard to have them force them.

Angela, we can say we're not taking tickets unless you put it through this route.

[@21:14](https://fathom.video/calls/560821416?timestamp=1274.62) \- **Gilbert, Channie (Bottomline Technologies)**

True. That will prompt them to prioritize, I'm sure, if it's an important ticket. Yeah. So we can do a little pushback on that.

You know, like, if this is not a break-fix, if this is not an urgent, and you're putting in a new answer request, put it in this way.

Right? I'm all for it. Because, I mean, again, if it's a priority, I'm pretty sure they'll make the time to put it through this process.

I don't know, who else do we have on the hook for this? Because I know we took Iglesa off, but who, do we have anyone?

And I know we can't do PayMode, and PayMode's what we could do. Ashish, we could have some PayMode 1.0 requests.

Yeah? Yeah. Yeah. Yeah.

[@22:01](https://fathom.video/calls/560821416?timestamp=1321.28) \- **\+19\*\*\*\*\*\*\*03**

Yeah, I agree.

[@22:02](https://fathom.video/calls/560821416?timestamp=1322.94) \- **Gilbert, Channie (Bottomline Technologies)**

Tiffany or Kendra, I don't know who does 1.0 for PayMode, but...

[@22:09](https://fathom.video/calls/560821416?timestamp=1329.36) \- **\+19\*\*\*\*\*\*\*03**

Kendra. Kendra.

[@22:11](https://fathom.video/calls/560821416?timestamp=1331.24) \- **Gilbert, Channie (Bottomline Technologies)**

Kendra. Okay, let's see.

[@22:12](https://fathom.video/calls/560821416?timestamp=1332.4) \- **Bresciani, Angela (Bottomline Technologies)**

have Tyler, Johnny, Lisa Hill, Kendra, Lizzie. Kendra.

[@22:17](https://fathom.video/calls/560821416?timestamp=1337.48) \- **Gilbert, Channie (Bottomline Technologies)**

Kendra. Kendra. Kendra. Kendra. Kendra.

[@22:19](https://fathom.video/calls/560821416?timestamp=1339.58) \- **Bresciani, Angela (Bottomline Technologies)**

Kendra. Kendra.

[@22:27](https://fathom.video/calls/560821416?timestamp=1347.7) \- **Gilbert, Channie (Bottomline Technologies)**

Kendra.

[@22:30](https://fathom.video/calls/560821416?timestamp=1350.14) \- **Bresciani, Angela (Bottomline Technologies)**

Kendra. Kendra. Kendra. Kendra. Kendra. Kendra. Kendra. Kendra. Kendra. Kendra.

[@22:37](https://fathom.video/calls/560821416?timestamp=1357.9) \- **Gilbert, Channie (Bottomline Technologies)**

Kendra. Kendra. Kendra. Kendra. Kendra. Kendra. Kendra. Kendra. And so if I'm going to defer, I will defer to you where the pressure we might want to lie, you know, or we want to hold off until we get a little more experience in there with it.

But if you do see an opportunity, maybe marketing, or I don't know who else we have on the list, but I would push back.

Maybe, maybe, maybe Candice, right? Maybe, I don't know. Yeah. I don't want to get drunk with Lisa either, so, you know, I don't want to push too hard on that one.

[@23:36](https://fathom.video/calls/560821416?timestamp=1416.34) \- **Smith, Sophie (Bottomline Technologies)**

They're very much a pair, those two. Yeah, I'm thinking maybe, because Bella Dixon seems to raise more and more these days, that could be a potential candidate for that.

**ACTION ITEM: Review business pilot list; add Bella Dixon; remove Candice Pridgin \- [WATCH](https://fathom.video/calls/560821416?timestamp=1423.9999)**

Do we have Bella on the list? No.

[@23:54](https://fathom.video/calls/560821416?timestamp=1434.16) \- **Bresciani, Angela (Bottomline Technologies)**

All right, let's talk about it offline.

[@23:57](https://fathom.video/calls/560821416?timestamp=1437.44) \- **\+19\*\*\*\*\*\*\*03**

Okay.

[@23:57](https://fathom.video/calls/560821416?timestamp=1437.72) \- **Bresciani, Angela (Bottomline Technologies)**

But yeah, we'll try to pull in.

[@23:59](https://fathom.video/calls/560821416?timestamp=1439.58) \- **Gilbert, Channie (Bottomline Technologies)**

Pull in.

[@24:00](https://fathom.video/calls/560821416?timestamp=1440.0) \- **Bresciani, Angela (Bottomline Technologies)**

We'll try to pull in more business users. Maybe have to give them an ultimatum. I guess, BAs, do you feel comfortable at this point in the current state to roll this out to business users, selected business users, or do you think we still need some more tweaks?

**ACTION ITEM: Find admin tickets for ExoHelp; route to Terry/Swanand; ask Melvin for feedback \- [WATCH](https://fathom.video/calls/560821416?timestamp=1455.9999)**

[@24:26](https://fathom.video/calls/560821416?timestamp=1466.34) \- **Smith, Sophie (Bottomline Technologies)**

I would be keen for more of our team to look at the detail first, potentially. I know we said Vishal and Nikita for kind of like the technical piece, but I've got a few that I've run through.

ExoHelp, not necessarily the impact analysis part, but just like what gets generated on the ticket in general could help.

I could, that could be helpful for the admins to look at, like I've got some with Melvin, I think.

So I could ask for some feedback from her. Yeah, are there at like BGSD admin? Do tickets that we can have them look at and give feedback, or?

[@25:04](https://fathom.video/calls/560821416?timestamp=1504.36) \- **Bresciani, Angela (Bottomline Technologies)**

Yes. Joe, Aashish, do you have any admin tickets that still need to be looked at? Maybe we can run those through AXO Help and pull in Terry or Swanand or someone to look at?

[@25:18](https://fathom.video/calls/560821416?timestamp=1518.8) \- **Vaillincourt, Joe (Bottomline Technologies)**

I don't have anything new, but I'm checking the unassigned to see if there's something. I mean, I have tickets, but I believe they're mostly 2.0.

[@25:30](https://fathom.video/calls/560821416?timestamp=1530.58) \- **Sharma, Aashish (Bottomline Technologies)**

I don't have that many 1.0.

[@25:32](https://fathom.video/calls/560821416?timestamp=1532.92) \- **Gilbert, Channie (Bottomline Technologies)**

Okay, no worries.

[@25:33](https://fathom.video/calls/560821416?timestamp=1533.86) \- **Sharma, Aashish (Bottomline Technologies)**

So I think that's where my kind of challenge comes in, is most of the tickets that we get for Paymote are mostly all 2.0.

[@25:40](https://fathom.video/calls/560821416?timestamp=1540.78) \- **Gilbert, Channie (Bottomline Technologies)**

But I'll take a look.

[@25:42](https://fathom.video/calls/560821416?timestamp=1542.36) \- **Sharma, Aashish (Bottomline Technologies)**

Okay, sounds good.

[@25:43](https://fathom.video/calls/560821416?timestamp=1543.86) \- **Bresciani, Angela (Bottomline Technologies)**

Hey guys, I'm just noticing that Candice that's on there, Pridgin, is not an appropriate person to have on this list.

[@25:51](https://fathom.video/calls/560821416?timestamp=1551.02) \- **Gilbert, Channie (Bottomline Technologies)**

We should take her off. No, I know. That's an old list, Shani. know it's- Oh, okay. Yeah, sorry. I pulled from an old list.

I was like, that's not the right person. Maybe we just switch around. I I don't know which one makes sense.

[@26:08](https://fathom.video/calls/560821416?timestamp=1568.36) \- **Smith, Sophie (Bottomline Technologies)**

We don't need to have them both in my mind. I don't know. I think it might be useful. I know they, they both like each other to be on various things.

So if we can have both, if that's okay, let's, let's just stick them both and we'll see.

[@26:23](https://fathom.video/calls/560821416?timestamp=1583.98) \- **Gilbert, Channie (Bottomline Technologies)**

Sophie, do you think there's any a use case where it would make sense to do this with CP, anyone from CPO?

[@26:35](https://fathom.video/calls/560821416?timestamp=1595.4) \- **Smith, Sophie (Bottomline Technologies)**

I don't know. I mean, potentially, they raise a hell of a lot of tickets for config. I know, that's why I was thinking of it.

pass a lot of that over, so that may not come in as much. I know, we're just going through a transition, yeah.

Yeah. Yeah. I don't think about it, though.

[@26:50](https://fathom.video/calls/560821416?timestamp=1610.58) \- **Gilbert, Channie (Bottomline Technologies)**

that's why we're kind of like, we're in a transition with them on what activities they're handling, so. Oh, nice.

That's why I was saying, I don't know if it makes sense at this moment. Yeah. So. yes. Yeah, I'll have a think.

[@27:03](https://fathom.video/calls/560821416?timestamp=1623.22) \- **Smith, Sophie (Bottomline Technologies)**

Yeah, there might be some kind of ad hoc ones that come in that may make sense. So I'll have a little look through the list.

All right, cool. Awesome. Hey, guys. Palomi Karthik, anything else?

[@27:19](https://fathom.video/calls/560821416?timestamp=1639.76) \- **Paulomi**

No, no, no. I think this is a great conversation. Thank you for the additional insights and feedback. I feel excited that we're starting to feel like we're moving forward and then that there's added value.

think the next kind of evolution of this is going to be exactly what you guys discussed in the last five minutes, which is figuring out more engagement.

And then the following step in the evolution is starting to see, you know, what are what what are we truly.

people need. So Saving in terms of time and effort and quality and really bringing, like, what's the KPIs that we're moving overall for this team to be able to really provide additional value to the business using ExoHelp.

So, that's where...

[@28:20](https://fathom.video/calls/560821416?timestamp=1700.1) \- **Bresciani, Angela (Bottomline Technologies)**

Sorry, I was just going to say, I think we've asked the BAs to kind of track the time savings, like, how long would this have taken you if you didn't have ExoHelp versus how long did it take, you know, to get?

[@28:31](https://fathom.video/calls/560821416?timestamp=1711.2) \- **Paulomi**

Yeah, I think there's one more variable, but there's time savings, and then there's actually, you know, and this is a longer term piece, so it's hard to measure, but I think the fact that you'll have a lot more documentation to look back on to see what changes have been made and why they were made and what happened and it just starts creating that repository for you, so that's a little bit more of an intangible output, but I think...

A lot more helpful in the long run. Awesome.

[@29:05](https://fathom.video/calls/560821416?timestamp=1745.72) \- **Bresciani, Angela (Bottomline Technologies)**

Cool. Thank you, guys. Well, enjoy your trip. If we don't talk to you, safe travels back, Paulomi. Oh, I'm back.

Oh, you are? Okay.

[@29:13](https://fathom.video/calls/560821416?timestamp=1753.48) \- **Paulomi**

I thought you were still traveling. I into the door. Okay. That's why I was taking the call from the car.

So I literally walked through the door and I'm home. Nice. Nice. Well, welcome home. Thank you. Thank All right, guys.

Thank you so much. Talk on Thursday. Thank you. everyone.

[@29:32](https://fathom.video/calls/560821416?timestamp=1772.42) \- **Vaillincourt, Joe (Bottomline Technologies)**

chatting. Thank you. you. Bye.

[@29:34](https://fathom.video/calls/560821416?timestamp=1774.5) \- **Gilbert, Channie (Bottomline Technologies)**

What's that?

[@29:35](https://fathom.video/calls/560821416?timestamp=1775.42) \- **Aravind Karthik (Realfast)**

Are we chatting next?

[@29:36](https://fathom.video/calls/560821416?timestamp=1776.94) \- **Paulomi**

Uh, sure.

[@29:37](https://fathom.video/calls/560821416?timestamp=1777.94) \- **Bresciani, Angela (Bottomline Technologies)**

Yeah, I had something with Allison, but yeah, let's Oh, you didn't say my name, right?

[@29:42](https://fathom.video/calls/560821416?timestamp=1782.34) \- **Gilbert, Channie (Bottomline Technologies)**

You can say. But I was like, I don't think that's what they said. Okay. Bye, guys. Bye. Bye.

[@29:57](https://fathom.video/calls/560821416?timestamp=1797.62) \- **Bresciani, Angela (Bottomline Technologies)**

I forget, Paulomi. I'm like, yes.

[@30:00](https://fathom.video/calls/560821416?timestamp=1800.0) \- **Paulomi**

She forwarded it to me, I don't always attend, but she's on vacation, so I'm like, hi, I am Allison for today.

So quick, quick just summary, I think, I'm hoping, I just wanted to give you a pulse check on the EXO help stuff.

It sounds like we're feeling okay overall. Yeah, I mean, anything else? No, I think it's going great.

[@30:24](https://fathom.video/calls/560821416?timestamp=1824.76) \- **Bresciani, Angela (Bottomline Technologies)**

I wish I could speed up, speed it up for you just to get more, you know, feedback for you, because obviously the quicker we get the feedback, the better.

It's just, yeah, it's just finding time, you know, and making it a priority for people on top of their day job.

So that's kind of my struggle, because I'm like, I want, I want Palomi to have what she needs, you know, so we can feel comfortable and, you know, open it up to more users.

[@30:52](https://fathom.video/calls/560821416?timestamp=1852.48) \- **Paulomi**

Yeah, I think that the approach that the team suggested makes sense, and I think we'll, it's cautious. you. Thank you.

Thank you. It's been optimistic at this point, so I'm okay with that. The second was the customer service side of the house, so we have our call on the 20th, right?

Thanks for setting that up.

[@31:17](https://fathom.video/calls/560821416?timestamp=1877.7) \- **Bresciani, Angela (Bottomline Technologies)**

Yeah, I wish I could do it this week, but yeah, that's the earliest I could get.

[@31:23](https://fathom.video/calls/560821416?timestamp=1883.58) \- **Paulomi**

It's okay, we'll work it through. So homework has been provided, I'm hoping that that'll kind of help us speed things up.

What do you think from a contract signing timeline perspective, because I was just debating, do I use the 20th almost as a kickoff, or do I, is it just more of a, like, hey, let's reconnect and make sure everything's going, like, how do I look at that?

**ACTION ITEM: Email Robert re: SOW/contract; confirm Feb 20 kickoff; route to Stephanie (AI buffer) \- [WATCH](https://fathom.video/calls/560821416?timestamp=1902.9999)**

[@31:53](https://fathom.video/calls/560821416?timestamp=1913.04) \- **Bresciani, Angela (Bottomline Technologies)**

Yeah, so let me get with Robert first and come back to you with an answer, because... He still hasn't confirmed that he's reviewed the S.O.W.

He was supposed to do it by Friday, last Friday, so I haven't heard anything, so let me, and he's on PTO next week, so I don't even know if he's going to be at that meeting, but whatever.

[@32:14](https://fathom.video/calls/560821416?timestamp=1934.5) \- **Paulomi**

We're still proceeding forward, honestly.

[@32:17](https://fathom.video/calls/560821416?timestamp=1937.36) \- **Bresciani, Angela (Bottomline Technologies)**

We have, like, his team can manage. doesn't, Robert doesn't need to be there. Let me ping him to sign me.

Okay. Let me see how he comes back. But yeah, that's a great question. So let's, let's see what Robert says.

If he's good, then yeah, why not use it as a kickoff? Hopefully you have the information you need by that time and a couple days, you know, before you get it a couple days before so you have time to assess it.

But can you confirm that you're able to access that SharePoint site? Because I know Allison was able to do it back when we used it for XO Help, but I'm not sure.

If you're able to do it, I put the link in the email, it's, it will take me a while, because I have to go through a lot of the, uh, all right, password, like, I, let me, I just, let yeah, get back to you on it.

Yeah, yeah, no worries. It's just easier to keep everything in one place than keep, you know, sending documentation via email and then getting it, um, just to confirm, it's in the email with the, sorry, it's in the meeting invite?

No, I put it, I sent an email, I hope I copied you, hold on, let me see, um, yesterday, um, when did I send it out, do, do, do, do, do, yeah, look at an email that I sent yesterday at 2.49pm, and it's called Service Assistant, yeah, see if you can get into that SharePoint site, because I'm asking everyone to put.

their documentation there.

[@34:07](https://fathom.video/calls/560821416?timestamp=2047.19) \- **Paulomi**

Let's see. I will know in a second. So much authentication going on. It's crazy. It's crazy. It's good. It's good.

It's necessary in this crazy world we live in. So.

[@34:39](https://fathom.video/calls/560821416?timestamp=2079.5) \- **Bresciani, Angela (Bottomline Technologies)**

Losing access to everything because they're just cracking down.

[@34:44](https://fathom.video/calls/560821416?timestamp=2084.92) \- **Paulomi**

So I got to the bottom line SharePoint and I had to request access. Okay. Let me see if I.

[@34:55](https://fathom.video/calls/560821416?timestamp=2095.3) \- **Bresciani, Angela (Bottomline Technologies)**

I didn't get an email yet.

[@35:02](https://fathom.video/calls/560821416?timestamp=2102.34) \- **Paulomi**

You need permission to access this item. Awaiting approval. We'll need to know about any updates. Okay. I don't know if that's coming to me or going to some other place.

[@35:12](https://fathom.video/calls/560821416?timestamp=2112.45) \- **Bresciani, Angela (Bottomline Technologies)**

So, oh, here we go. I got the email. Okay, so I am approving it. Just try it back in a second.

Just give it a second.

[@35:32](https://fathom.video/calls/560821416?timestamp=2132.47) \- **Paulomi**

Okay.

[@35:32](https://fathom.video/calls/560821416?timestamp=2132.95) \- **Bresciani, Angela (Bottomline Technologies)**

While you're waiting to look at that, one of the other things that we would like to start, one of the AI use cases assigned to the team was creating an internal knowledge base.

And we may have talked about this or not, so it might be repetitive. But is there a way to, to your point in the last meeting, hey, we're building all this great documentation in JIRA.

Can we build a knowledge base? Is base for our internal team to leverage that? A knowledge base of Salesforce?

[@36:08](https://fathom.video/calls/560821416?timestamp=2168.72) \- **Paulomi**

No, Jira content. Right, but it's Jira content. Or Salesforce. What's that? Sorry, I'm a little confused as to what knowledge base you're thinking about building.

Is it for sales? Like, it's a knowledge base on, not on Salesforce, about Salesforce that comes out of the Jira tickets?

No.

[@36:34](https://fathom.video/calls/560821416?timestamp=2194.29) \- **Bresciani, Angela (Bottomline Technologies)**

It's more for, it's more for our internal team to be able to look up, I don't know, like, users asking, you know, XYZ, how do we do this?

Just like based on all the knowledge of solutioning and requests coming through Jira, you know, building that, you know, knowledge base so people on our team can vs.

view 나서, Ask questions based on what, you know, we've done in the past. So it wouldn't be open to our business users within Salesforce.

It would just be for our internal admins, BAs, developers to have some kind of knowledge base.

[@37:14](https://fathom.video/calls/560821416?timestamp=2234.89) \- **Paulomi**

Or any application in addition to Salesforce? Is that how you're thinking?

[@37:22](https://fathom.video/calls/560821416?timestamp=2242.19) \- **Bresciani, Angela (Bottomline Technologies)**

Just based on all the tickets that come through, like, and the documentation of solutioning and, you know, how we...

implemented things or developed things, we would have that through a knowledge base.

[@37:36](https://fathom.video/calls/560821416?timestamp=2256.79) \- **Paulomi**

Okay.

[@37:37](https://fathom.video/calls/560821416?timestamp=2257.37) \- **Bresciani, Angela (Bottomline Technologies)**

Because you said, like, we're building all this documentation. Well, how are we going to leverage the documentation if we don't have some kind of search engine or, you know what I mean?

Like, how would we leverage that? I'll tell you how I was thinking about it over time.

[@37:49](https://fathom.video/calls/560821416?timestamp=2269.83) \- **Paulomi**

Okay. Sure. So there's two, there's multiple components to this in my head. One, the way I was thinking about it is the way I've seen many organizations...

was about just to and, and, and... Manage change in Salesforce is, especially code-based changes and flow-based changes, things like that, that are kind of buried.

They, and even config sometimes, they reference the JIRA ticket number for that code base to then, like, if someone's looking like, okay, what's happening?

Like, if I look this code, why did we do this? Okay, let's go look in that JIRA ticket app.

So now you have just a lot of content in that JIRA ticket of, like, what, what was done. So that's how I was actually thinking about it.

To your question of, like, people being able to ask about, like, what about this, right? We are actually, and this is a totally different approach.

We are kind of setting up a way to. Talk to your Salesforce org and ask it the same types of questions that you're kind of suggesting.

Instead of looking at the content of Jira, it's almost like looking at the Salesforce configuration and asking, like, what is going on here and being able to ask the org directly as if you can talk to it.

So, if you actually look at, and I'll have to double check with the team and talk to Karthik about it, but there's a, there's, now I think we've exposed it, all of our XOs, not all, but some of our XOs to you.

One is XO Help, one is XO Web, and I think we have an XO Help Pro exposed to you.

So, XO Web is actually the ability to talk to your org and ask those questions, which is, like, over and above everything else we're doing, but it's...

One of our other products that we're starting to build out. So, that might be something, I think, along the lines of what you're asking about.

But if you truly still need something as a knowledge repository on top of JIRA, we could do that. It would be a different project, but we could totally do that.

Would it be something easy to do?

[@40:25](https://fathom.video/calls/560821416?timestamp=2425.73) \- **Bresciani, Angela (Bottomline Technologies)**

Because we're kind of trying to experiment, excuse me, internally using CoPilot. I don't even know how that would work, but how easy that would be.

But if you guys, since, you know, the ExoHelp is, like you said, building the knowledge anyways, like, maybe it's easier for you guys to do it.

I don't know. I'm just kind of, like, spitting out ideas. Yeah, no.

[@40:50](https://fathom.video/calls/560821416?timestamp=2450.35) \- **Paulomi**

So, to be candid, I think because of your security pilot policies, CoPilot might have an easier act. I don't like You would think, right?

[@41:04](https://fathom.video/calls/560821416?timestamp=2464.61) \- **Bresciani, Angela (Bottomline Technologies)**

We still have to go through a rigorous security approval, anything we do with CoPilot.

[@41:11](https://fathom.video/calls/560821416?timestamp=2471.17) \- **Paulomi**

My concern, though, is CoPilot isn't always great with its answers. That's what I'm experiencing, yeah. I don't like it.

And we don't use, I mean, for that reason, we don't use it because we're like, this just gives you, it doesn't give you what you want.

And to get what you want out of it, you have to, there's a whole bunch of, I mean, let me rephrase it.

Even if you try to get what you want out of it and work at, like, really structuring the content and the prompts and everything, it's still lackluster.

So, that's why we've moved into, like, the, like, underlying technology is Claude. So... So... So... It's not, it's not a quick thing, but let me take it back and we, you know, my team and I can brainstorm and see what we can do.

[@42:09](https://fathom.video/calls/560821416?timestamp=2529.97) \- **Bresciani, Angela (Bottomline Technologies)**

I mean, maybe it's too early. Maybe we need to let some time pass. So, you know, let, let us go through the EXO help.

Let's get more knowledge in there, you know, underlying documents or whatever, like knowledge, whatever is produced from the EXO help process.

[@42:26](https://fathom.video/calls/560821416?timestamp=2546.81) \- **Paulomi**

Yeah.

[@42:27](https://fathom.video/calls/560821416?timestamp=2547.35) \- **Bresciani, Angela (Bottomline Technologies)**

But yes, that's something that we definitely want to look into because what good is building the documentation if we can't have a good way to access it accurately?

Yeah.

[@42:37](https://fathom.video/calls/560821416?timestamp=2557.61) \- **Paulomi**

As I said, there's a whole process of like where I've seen many organizations just reference the ticket number itself in the code base as comments.

I like, yeah, I didn't know that.

[@42:47](https://fathom.video/calls/560821416?timestamp=2567.83) \- **Bresciani, Angela (Bottomline Technologies)**

That's, that's actually really good to know. That would be super then it's self-documenting.

[@42:52](https://fathom.video/calls/560821416?timestamp=2572.29) \- **Paulomi**

Yeah. Then it becomes self-documenting overall. So. Interesting. I would even start there because. I'll Then, you know, the minute you want to look at some section of some code, it's like, oh, yeah, we did this last year.

And here's the whole reason why we did this. Absolutely.

[@43:11](https://fathom.video/calls/560821416?timestamp=2591.27) \- **Bresciani, Angela (Bottomline Technologies)**

While I have you, so there's a huge, huge, huge push and pressure on Robert to come up with more customer support, you know, AI opportunities.

So, can you help us go even beyond what's brought to you as far as their use cases, like, and just think like, hey, Robert, what about this?

What about this? What about this is what other companies are doing?

[@43:47](https://fathom.video/calls/560821416?timestamp=2627.35) \- **Paulomi**

So, can we, so I actually, it's so interesting you say that. So, while I was there with the team, we were trying to think how to approach a lot of things.

we, so And one of the things, sorry, my battery's running low, one of the things we were thinking, and we on, hold on, Paulomi, I'm inviting you, Daryl, because he probably wants to hear this too, because he was on that meeting, and he was just trying to call me, but now he's not picking up.

He doesn't like us. Oh, there he is. I was just saying, Daryl, you don't like us. How rude, you're not picking up the phone.

[@44:31](https://fathom.video/calls/560821416?timestamp=2671.31) \- **Bresciani, Angela (Bottomline Technologies)**

Yeah. I had a feeling while you were calling me, and ironically, I'm talking to Paulomi, and I just kind of am debriefing her on our Emergency AI Council meeting this morning.

Well, I think that was poorly labeled, by the way.

[@44:44](https://fathom.video/calls/560821416?timestamp=2684.51) \- **Padilla, Yaderl**

That was a little bit of a long list, but emergency.

[@44:48](https://fathom.video/calls/560821416?timestamp=2688.05) \- **Bresciani, Angela (Bottomline Technologies)**

But, you know, so I posed the question, I'm like, what else aren't we thinking about, Paulomi? How can you help us?

So, and she was just about to answer the question. I said, wait, Daryl's joining. Hold on. So, go ahead.

Hopefully your battery doesn't...

[@45:00](https://fathom.video/calls/560821416?timestamp=2700.01) \- **Paulomi**

No, I just plugged in, so it's good. Oh, So, this is another – so, I was in meeting with the team all week last week.

So, we obviously were working through our strategy for the next year, and one of the strategies that we're working through is we're seeing the world, and, you know, bottom line is no different than everyone else out there.

We're trying to embrace AI has been hard because a lot of ways to embrace AI requires you to rethink your existing kind of worldview and processes.

So, we took a step back and said, hey, how are most organizations historically kind of doing this, and, you know, what do they do?

So, let's Let's So, historically, a lot of organizations would bring in the BCGs, the McKenzies of the world to say, okay, what, you know, talk to us about how we should review or re-engineer our business to meet the future needs.

And then they would give you a whole bunch of recommendations and then you'd have to find an implementation company to do whatever the recommendations they are.

So, this is my long-winded way of, we're looking to actually build out an arm of that AI transformation conversation in the team, because we actually have a bunch of McKenzie, ex-McKenzie people who just have done this as their kind of bread and butter before.

Um, just, it's an interesting group of people that Realfast is put together. Um, so. So. My long-winded way of saying, hey, this is how I'm thinking about this, is the next phase of what I think for support we'd have to look at, because we've historically looked at it very tactically, like, look at this case type and look at this and what is this, is possibly taking a step back and saying, let us have an over-the-shoulder period with your service agent.

Let us look at what they're doing. Let us analyze what they're doing. Let us do some process mapping for what they are actually doing so that we can help with re-thinking what their future processes would look like.

And then give you recommendations of AI, because otherwise, all I'm doing is throwing spaghetti at the wall of all of the different technologies and features that are out there and having the team, like, say, maybe, maybe not.

And hopefully, as part of the process investigation, we can also help with some of the ROI conversations, because as part of that kind of investigation, we're gathering context for that.

So, does that answer your question? Does that give you the ammunition that you're looking for?

[@48:27](https://fathom.video/calls/560821416?timestamp=2907.53) \- **Bresciani, Angela (Bottomline Technologies)**

Yeah, I mean, yeah, go ahead, Yadav.

[@48:32](https://fathom.video/calls/560821416?timestamp=2912.05) \- **Padilla, Yaderl**

Yeah, you know, I think the, so here's the deal. mean, again, like emergency, like all that, we can just throw that in the trash for a second.

But I think the question is, you know, do we really have a vision for AI and customer support? Because the belief is that...

that... that... Is That is an area where we have an opportunity. Why? Because everyone else has seen the opportunity.

And now the Tomo Bravo portfolio companies are coming back and claiming wins that we're not claiming. So the push came from the executive leadership team, like, all right, what is it?

What's holding you back? You got a plan. Let's make it happen. You know, that sort of thing. So that's the call to action, right?

Is we need to get to a vision with some clear objectives, measurable objective, and a plan. So I think that that's what you're saying, Paulomi, could probably help us in that area, you know?

You know, know, there's, where I struggle a little bit is I think that there's some work that we need to do ourselves first.

[@49:59](https://fathom.video/calls/560821416?timestamp=2999.49) \- **Paulomi**

First.

[@50:01](https://fathom.video/calls/560821416?timestamp=3001.15) \- **Padilla, Yaderl**

Before the army of smart people shows up to do over the shoulders and analyze our world, you know, someone needs to set a vision for support, you know, someone needs to set some metrics, some, you know, things that we're all sort of aiming towards, and that's where I'm trying to get Rob to focus.

It's just like, put the technology aside for a second, you know, what are, what are those big problem statements, what are those big outcomes, what are those kind of big business objectives, I guess, you know, what is that, you know, because I don't, I don't want to just throw energy at a, at a car that's going in the wrong direction.

[@50:55](https://fathom.video/calls/560821416?timestamp=3055.85) \- **Paulomi**

I get it, I get it, um, if I can be candid. And I think that's where he needs some help to form those spots.

That makes me sad. Of where I think you're right. Goals need to be. And, you know, this is, as I said, you guys don't know, this is exactly where we're seeing the world go.

It's like no one actually just knows what those things are. Like, and the only way you could do this is right now, as a service organization, you just say, okay, I have, you know, average handle times of X and first call resolution of Y.

want to move X to, you know, A and Y to Z. Like, you could do the old standards and you could have those metrics defined and that's easy enough.

I mean, that you could do tomorrow and say, this is what I want to move. These are the things I want to move.

And then you come back and say, okay, now that I want Now that I have those goals, what processes do I have to touch to move those, like, adjust those goals, right?

And if you're asking about that, then there's, like, in the service organization, there's, like, maybe four or five key metrics that every organization just measures.

That's not complicated. But then it's, like, how, once you've gotten those goals defined, how do you move those goals?

Like, how do you move towards those goals? Is, is the whole process re-engineering and evaluation piece is what I'm talking about at that point.

[@52:36](https://fathom.video/calls/560821416?timestamp=3156.61) \- **Padilla, Yaderl**

what, yeah, so what would something like that look like? In terms of what, timing, cost?

[@52:44](https://fathom.video/calls/560821416?timestamp=3164.61) \- **Paulomi**

All of it, I guess, right?

[@52:48](https://fathom.video/calls/560821416?timestamp=3168.17) \- **Padilla, Yaderl**

yeah, how do we size, how do we scope something like this? You know, we need a vision for, we need a target state, and we need a plan to get there.

Mm-hmm.-hmm. Mm

[@53:00](https://fathom.video/calls/560821416?timestamp=3180.67) \- **Paulomi**

Yeah.

[@53:01](https://fathom.video/calls/560821416?timestamp=3181.21) \- **Padilla, Yaderl**

So, all the ingredients that go into that. I'm telling you what we just discussed last week.

[@53:08](https://fathom.video/calls/560821416?timestamp=3188.39) \- **Paulomi**

I don't have a number right now. No, I'm asking for a number.

[@53:12](https://fathom.video/calls/560821416?timestamp=3192.75) \- **Padilla, Yaderl**

I'm almost like saying, okay, if you're ready to talk to us about it, like, how do we, how do we, what's the next, what's the next step?

Like, how do we kind of make this more real? You know, and maybe if you need to go back and think about it, that's cool.

I'm not joking. I'm not trying to do weird or natural things, but I'm just trying to get some, you know, where we are today, how could this help us, and then what needs to be true for us to get the help kind of thing.

**ACTION ITEM: Draft Service Assistant AI transformation playbook; share w/ Angela/Daryl \- [WATCH](https://fathom.video/calls/560821416?timestamp=3211.9999)**

[@53:42](https://fathom.video/calls/560821416?timestamp=3222.83) \- **Paulomi**

Let me, let me work with the person on my team who's actually putting this team together. Yeah. And get a plan because in my mind, what you're asking for is the recipe book.

So, Thank or the approach we would take to get you from point A to point B. That is it.

Right? So, if I, you know, and then we just outline like, we need to, we need access to A, B, and C people, we need to review, you know, over the shoulders for this many days and weeks, and then once we have that, we, these are the kinds of recommendations you can expect from us, and then we move forward.

That's it.

[@54:28](https://fathom.video/calls/560821416?timestamp=3268.47) \- **Padilla, Yaderl**

That's it. Just the playbook. Or the recipe book. It's that. Yeah. Okay.

[@54:36](https://fathom.video/calls/560821416?timestamp=3276.39) \- **Paulomi**

Give me a couple of days. I will come back to you on that and figure out what that would look like as an engagement.

Because I, I honestly, I can't see a world where you, you continue to try to use the technology without knowing how to change the process.

Because that's what is very clear to me right now. No, certainly.

[@55:01](https://fathom.video/calls/560821416?timestamp=3301.79) \- **Padilla, Yaderl**

And I, and we, I still think that there are parts of this that maybe you can, um, you can, you can ask the right questions to get us thinking, but we still have work to do ourselves, like.

You do. And I'll tell you what the biggest one you have is your knowledge base cleanup.

[@55:21](https://fathom.video/calls/560821416?timestamp=3321.27) \- **Paulomi**

I don't know where that stands. Yeah. Um, and you know, I think that's, that's a challenge until you get that in place and you're, you're a customer cube, because without a lot of that data insights, I think your self-service part of the customer support side is, is crippled and being able to know what a customer even has before you can actually help them is crippled.

So, I mean, in my mind, in the last couple of months, that's kind of what I've seen as the big, big two that is slowing you guys down, that really no one can really help you with.

So you do it. Yeah. No, that makes sense.

[@56:07](https://fathom.video/calls/560821416?timestamp=3367.07) \- **Bresciani, Angela (Bottomline Technologies)**

Okay. Well, I just give you a heads up. So we're making really good progress with ExoHelp, Daryl, and getting the feedback.

But one of the challenges is really having the business pilot users carve time and make this a priority, too.

So, Shannie's like, let's give them an ultimatum. They can't enter any tickets unless they're using ExoHelp type thing. So that way we force the feedback, but we'll figure it out.

But, yeah.

[@56:37](https://fathom.video/calls/560821416?timestamp=3397.63) \- **Padilla, Yaderl**

said, hold on, did people commit and then they're not, like, did people say yes and now they're not doing the thing that they said they were going to do?

Yeah.

[@56:47](https://fathom.video/calls/560821416?timestamp=3407.03) \- **Bresciani, Angela (Bottomline Technologies)**

Cool. Cool. Well, Tyler, only because of medical reasons he's been out. So he's had to kind of pick and choose what he works on because he's working a limited schedule.

**ACTION ITEM: Reject non-ExoHelp tickets from pilot users (Tyler, Johnny, Matt, Kendra, Lisa, Lizzie) \- [WATCH](https://fathom.video/calls/560821416?timestamp=3419.9999)**

But... We just opened it up to, like, Matt Jones, Johnny, some other people, um, within the last week, so, just need to, uh, So they said yes, they said yes, we're gonna do it, right?

they haven't touched it. Reject their tickets. That's what, that's what Channie said, like, yeah. Yeah, just reject their tickets.

I mean, if they said they were gonna do it one way, then why are they doing it the other way, so.

Yeah, yeah, yeah. So, I'm just, we're just trying to get the feedback that Palomi needs, um. Yeah, reject their tickets.

Okay. All right. I think you go, go do it right now if you can.

[@57:32](https://fathom.video/calls/560821416?timestamp=3452.07) \- **Padilla, Yaderl**

I mean, mean, you know, what are you gonna try to convince people to stick to their commitments? I think everyone was an adult with a paycheck.

Cool.

[@57:43](https://fathom.video/calls/560821416?timestamp=3463.67) \- **Bresciani, Angela (Bottomline Technologies)**

Will do. You heard that, Palomi. Have you, Daryl's permission.

[@57:48](https://fathom.video/calls/560821416?timestamp=3468.13) \- **Paulomi**

You're my witness.

[@57:49](https://fathom.video/calls/560821416?timestamp=3469.33) \- **Padilla, Yaderl**

Yeah, I mean, Palomi, mean, I'm, I'm, to Palomi, I'm, um, uh, she would probably say, I'm too soft, you know?

[@58:00](https://fathom.video/calls/560821416?timestamp=3480.01) \- **Paulomi**

I guess I had to go compared to Palomi.

[@58:02](https://fathom.video/calls/560821416?timestamp=3482.97) \- **Bresciani, Angela (Bottomline Technologies)**

Uh, all right. Cool. I don't even register on the Palomi scale.

[@58:11](https://fathom.video/calls/560821416?timestamp=3491.05) \- **Paulomi**

Yeah.

[@58:12](https://fathom.video/calls/560821416?timestamp=3492.71) \- **Bresciani, Angela (Bottomline Technologies)**

So let us know, I guess, Palomi, what your thoughts are once you meet with the person on your team.

So, yeah, I'll get back to you on that.

[@58:21](https://fathom.video/calls/560821416?timestamp=3501.31) \- **Padilla, Yaderl**

Yeah, we're going to continue doing our pieces, too, because I want to get the wheels turning on things. Palomi, I have a, this is a separate ask, maybe just more of an idea.

Maybe you have some thoughts. If we want us to, if we wanted to staff up internally, you know, an AI team, and really, like, the way I'm kind of sort of thinking about it is you have the data side of it, right?

Okay. So we want some of that, too. We're putting that. I'm for a second, but more like the understanding that there are data dependencies all over the place, right?

Like I get that, but more of like the generative automation side of it, are there like roles in your company or anywhere else?

Like, like, how do you guys hire for that? I'm interested in like job descriptions or something, some clues around that, because that's an idea that I'm been kicking around with some folks and it's like, alright, well, if I can go get them, what am I looking for?

know?

[@59:40](https://fathom.video/calls/560821416?timestamp=3580.61) \- **Paulomi**

Um, forward deployed engineers is the, is the job, you know, fashion statement of the year. Who deployed engineers?

[@59:55](https://fathom.video/calls/560821416?timestamp=3595.95) \- **Padilla, Yaderl**

Isn't that what the, isn't that what the guy at Microsoft was saying the other day? They, uh,

[@1:00:00](https://fathom.video/calls/560821416?timestamp=3600.01) \- **Paulomi**

Palantir. Oh, Palantir. Palantir. Palantir, okay. Yeah. What's it called?

[@1:00:06](https://fathom.video/calls/560821416?timestamp=3606.31) \- **Bresciani, Angela (Bottomline Technologies)**

I didn't catch the first word. Forward?

[@1:00:09](https://fathom.video/calls/560821416?timestamp=3609.51) \- **Paulomi**

Oh, forward. Forward. Engineers.

[@1:00:14](https://fathom.video/calls/560821416?timestamp=3614.13) \- **Padilla, Yaderl**

Okay. And what is a forward deployed engineer? What I've heard is like it's a combination of product management, development, and something else.

[@1:00:24](https://fathom.video/calls/560821416?timestamp=3624.15) \- **Paulomi**

Yeah. I mean, it really comes down to people who can be... somewhat consultative, i.e. the product management piece, understand the business challenges, and apply the tech because they're extremely technical also.

Like, they're engineers, but they're forward because you're in front of the customers. Historically, engineers were behind, so that's why the word forward is there, and they're deployed because, you know, they're interacting.

So, you take those two personalities and you make the... into a single person, and that's your forward deployed engineer.

The key difference in this AI world is they have a good understanding of obviously business issues, integrations is a good big piece of it, and data architecture, data architecture integrations, and then AI application to those things.

Once you have those three together, um, you kind of have your secret person, finding those secret people, finding those secret people is hard, very, very expensive, that's a lot, yeah, yeah, it's hard, okay, no, I'm just, just Google search, wow, enlightening, okay, um, yeah, yeah, yeah, there you go.

[@1:01:50](https://fathom.video/calls/560821416?timestamp=3710.67) \- **Padilla, Yaderl**

They bridge the gap between product capabilities and user needs.

[@1:01:55](https://fathom.video/calls/560821416?timestamp=3715.65) \- **Paulomi**

Mm-hmm, and just, you know, they're, they're, they're drill, what your drill is.

[@1:02:02](https://fathom.video/calls/560821416?timestamp=3722.95) \- **Padilla, Yaderl**

What I've done so poorly for this version kind of does it well, you know, minor distinction. Okay, cool, cool.

Thank you for that tip.

[@1:02:18](https://fathom.video/calls/560821416?timestamp=3738.23) \- **Paulomi**

I'll look around. Yeah, yeah, no, for sure, for sure. And if you, if you want to chat some more, let me know about that.

Yeah, I will do that.

[@1:02:30](https://fathom.video/calls/560821416?timestamp=3750.93) \- **Bresciani, Angela (Bottomline Technologies)**

I'll shoot some ideas your way. Go ahead. I know we're over time, but, um, so I will get Robert to confirm, Paulomi, about the Service Assistant.

SOW will get that through the procurement process. Yadaryl, any hesitation there, or? No. Okay. No, tell Stephanie that that comes out of the AI buffer, too.

[@1:02:49](https://fathom.video/calls/560821416?timestamp=3769.47) \- **Padilla, Yaderl**

Well, I like having an AI buffer.

[@1:02:52](https://fathom.video/calls/560821416?timestamp=3772.99) \- **Bresciani, Angela (Bottomline Technologies)**

Well, that's it, we've exhausted it. I know, I was going to say, we're going to go through that very quickly.

[@1:02:58](https://fathom.video/calls/560821416?timestamp=3778.03) \- **Paulomi**

All right, cool. And then, um. Um, no.

[@1:03:00](https://fathom.video/calls/560821416?timestamp=3780.01) \- **Bresciani, Angela (Bottomline Technologies)**

Problem on URN, Paulomi, adding additional product segments for Service Assistant, right? It just increases the scope, but the solution is going to be the same, right?

[@1:03:10](https://fathom.video/calls/560821416?timestamp=3790.13) \- **Paulomi**

The solution is the same, but I mean, Service Assistant is a platform, right? It's like flow. You just keep on adding all of it, so it's fine.

Awesome. Cool. Well, glad you had you. you, Daryl.

[@1:03:23](https://fathom.video/calls/560821416?timestamp=3803.43) \- **Bresciani, Angela (Bottomline Technologies)**

Did you need me for anything else? Bye, Paulomi. Thank you. All right. Take care, Paulomi. Thanks, guys.

[@1:03:30](https://fathom.video/calls/560821416?timestamp=3810.13) \- **Paulomi**

Thank you.

[@1:03:31](https://fathom.video/calls/560821416?timestamp=3811.09) \- **Padilla, Yaderl**

I sent you the link to all the notes that the facilitator took. Yes. I haven't looked at it yet.

[@1:03:39](https://fathom.video/calls/560821416?timestamp=3819.27) \- **Bresciani, Angela (Bottomline Technologies)**

So good. That thing is so good. You know, it's funny, before you join the call, I said, Kevin, we should record this.

And he's like, no, I can take notes. I'm like, okay. Like, why wouldn't you use, especially since we're talking about AI, you don't want to record this meeting and get the AI notes.

Maybe he doesn't have a proof. Does he

[@1:04:00](https://fathom.video/calls/560821416?timestamp=3840.01) \- **Padilla, Yaderl**

No, does.

[@1:04:01](https://fathom.video/calls/560821416?timestamp=3841.65) \- **Bresciani, Angela (Bottomline Technologies)**

I think he does, yeah. He's recorded meetings in the past. Maybe because it was an emergency meeting, he thought it was like top secret or something.

I don't know. Yeah, I don't know anything about that guy.

**ACTION ITEM: Own Emergency AI Council use cases and action items \- [WATCH](https://fathom.video/calls/560821416?timestamp=3859.9999)**

[@1:04:15](https://fathom.video/calls/560821416?timestamp=3855.41) \- **Padilla, Yaderl**

The only thing I know is he just added me to a bunch of meetings and I declined them. Yeah.

[@1:04:20](https://fathom.video/calls/560821416?timestamp=3860.91) \- **Bresciani, Angela (Bottomline Technologies)**

We're being recorded, by the way, because this was XO Help. That's okay. Yeah, okay. This was our XO Help call, so we just continued.

[@1:04:30](https://fathom.video/calls/560821416?timestamp=3870.53) \- **Padilla, Yaderl**

So what I wanted to do was, what I wanted to do was to, you know, the lists that we, the action items and all that stuff, I think we need to take over, right, for them, walking it forward.

[@1:04:49](https://fathom.video/calls/560821416?timestamp=3889.07) \- **Bresciani, Angela (Bottomline Technologies)**

So if you look at the use cases and action items there, if you could kind of own, if you could just own moving it along.

