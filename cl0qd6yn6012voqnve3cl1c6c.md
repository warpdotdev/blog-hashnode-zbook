## Planning

<p>So you’ve decided on the general outlines of what you want to build. &nbsp;You have an engineering team, designers, PMs.  It’s time to figure out who works on what, what order to build things in, what you are really building, and so on. &nbsp;It’s time to get to the nitty gritty of building a product.<br></p>

<p>What’s the best way to actually do this? &nbsp;There are a lot of methodologies out there &#8211; agile, scrum, kanban, waterfall, and so on. &nbsp;I don’t really subscribe to any of them, but instead I can tell you the general outlines of what I’ve done in the past, some principals that work, some pitfalls to look out for.<br></p>


## OKRs

<p>Let’s start with the question of goal setting. &nbsp;<br></p>

<p>A good practice that I took away from Google is starting with quarterly <a href="https://en.wikipedia.org/wiki/OKR">OKR</a>s. &nbsp;OKRs stand for “objectives and key results.” &nbsp;You make a list of the things you want the team to get done (e.g. improve onboarding) and for each one of those things specify the metric that lets you measure it (e.g. % of users who complete onboarding goes from 60% to 80%). &nbsp;<br></p>

<p>These Objectives should generally be <em>outcome</em> driven goals (e.g. improve performance, improve conversion, improve customer satisfaction) rather than <em>output</em> goals (e.g. minimize JS, put button in a different spot on page; add chat widget to homepage). &nbsp;<br></p>

<p>The Key Results can be numeric metrics (if possible) or output oriented if it’s not yet possible to attach a reasonable number to the goal. &nbsp;If you are too early in your development process then the result you are shooting for might just be building and launching the thing, rather than moving a metric. <br></p>

<p>Here are some OKRs from my last company:<br></p>

<ul><li><strong>Improve our ability to edit photos to match a customer’s brand</strong><ul><li>Increase positive outcome rate to 70%</li><li>Reduce revisions citing &#8220;Doesn&#8217;t match style&#8221; to 3%</li></ul></li><li><strong>Improve the performance of our image specialists</strong><ul><li>Increase positive outcome rate to 70%</li><li>Reduce revisions citing &#8220;Looks fake&#8221; or &#8220;Didn&#8217;t follow my instructions&#8221; to 10%</li></ul></li><li><strong>Improve the growth rate of our customers and their engagement in our app</strong><ul><li>Increase % of members using the planner weekly to 50%</li><li>Increase median time in app to 4:00</li><li>Increase members&#8217; followers by 10% MoM (median)</li></ul></li></ul>

<p>Notice that we were going for very specific changes in metrics. &nbsp;I’ll speak more to the question of whether you should be prioritizing completing features or driving customer outcomes in a bit.<br></p>

<p>You make this list at the beginning of the quarter and spend the next three months working on it and tracking your progress. &nbsp;You’ll want to check on how you are tracking on these goals every month at a minimum.  Importantly, at the end of the quarter, before making your next list you go back and grade yourself on how you did on the last one. &nbsp;<br></p>

<p>The grades should be pretty high-level; I like to use a green/yellow/red framework: green = you nailed it; yellow = some progress but incomplete; red = you missed it. &nbsp;The grading keeps you accountable to yourself and the rest of the company.<br></p>

<p>Quarterly OKRs should not appear out of thin air as a diktat of a single product leader. &nbsp;&nbsp;Instead there should be a collaborative process for arriving at them.  The exact process doesn’t matter that much, but it needs to synthesize data from a lot of different points.<br></p>

<p>Those data points ideally include input from users, engineers, PMs, designers, sales, marketing, and other stakeholders. &nbsp;Common ways of getting this data are surveys, retros, feedback-emails, bug reports, NPS surveys, etc.<br></p>

<p>Good ideas come from everywhere and gathering input with a wide net is a good idea. &nbsp;But, at the end of the day, someone needs to decide what the real priorities are and be able to justify them to the larger team. &nbsp;<br></p>

<p>Deciding what not to do is just as important as deciding what to do.<br></p>

<p>At a small startup the ultimate decider is the CEO or CTO. &nbsp;At a bigger one it might be a VP of Product or Engineering.  At a place like Google it’s typically the tech lead, eng manager or PM. &nbsp;OKRs roll up through an organization, so there will be OKRs of increasing scope the higher up in the org you get.<br></p>

<p>The way the decider should pick what to work on is by looking at a lot of different factors and arriving at a stack rank. &nbsp;Then you choose as many of the items from the top of the list as you have resources to get done.<br></p>

<p>And these decisions should happen pretty quickly. &nbsp;If you are spending more than a week or at most two deciding on what to work on, then you are spending too long. &nbsp;You need to <a href="https://www.fastcompany.com/3049164/how-to-make-decisions-more-efficiently">move fast</a>.<br></p>

<p>Which brings me to the topic of prioritization…<br></p>

## Prioritization

<p>I’ve had to prioritize a lot of projects and the only thing I’m certain of on the topic is that no matter how you prioritize someone is going to think you are doing it wrong. &nbsp;<br></p>

<p>To start, let’s admit that prioritization is a hard problem, and you are not going to come up with a perfect solution. You will never know if the priority order you came up with was the right one. &nbsp;<br></p>

<p>The best you can do is use a reasonable framework and come up with your best guess and get on with building. &nbsp;<br></p>

<p>That said, it’s good to start by judging candidate projects along a few big dimensions:</p>

<ul><li><strong>Impact</strong>: how big of a deal will it be if you get the project done &#8211; how much does it help you hit the OKR?</li><li><strong>Effort</strong>: How much work is it? How long will it take?</li><li><strong>Risk</strong>: Can you actually build it? &nbsp;And, if you do, are you sure it will achieve the desired outcome?</li><li><strong>Definition</strong>: How scoped is the work? &nbsp;Do you actually know what you want to build?</li><li><strong>Resources</strong>: Do you have the right resources available to work on the project?</li></ul>

<p>E.g. say you are building an asset library for a photo editing tool. &nbsp;You might weigh one feature that lets users find content on the web and upload it themselves against another that uses machine learning to find and identify content. &nbsp;The first would probably be lower risk and lower effort, but also lower impact.  The second (the ML solution) could be risky, take longer and be harder to scope but might have a bigger payoff. &nbsp;It also might require special resources in terms of engineering talent and data.<br></p>

<p>The goal, per above, is to make sure you hit the OKRs. &nbsp;Typically you do this by maximizing impact and reducing effort and risk. &nbsp;In our hypothetical asset library example you would weigh the difference in impact, effort, etc and make a judgement call on whether the extra risk and effort was worth the payoff.<br></p>


## The Real World is Messy

<p>In the real world though things are rarely so simple and if you do prioritization just based on the above, you’re likely to land in a world of pain. &nbsp;There are other things to consider…<br></p>

<p>You need to make sure the engineers on the team are <strong>happy</strong> and working on things they find interesting. &nbsp;If you don’t you may have attrition.  You also will have less productivity as engineers stop working as hard, start coming in late, feel demotivated and so on. &nbsp;You want <a href="https://svpg.com/missionaries-vs-mercenaries/">missionaries not mercenaries</a> on your team.<br></p>

<p>You need to make sure that engineers are on a <strong>growth path</strong> and being prepared for promotion at some point. &nbsp;Every engineer wants better skills, a higher salary, and more responsibility. &nbsp;Some projects lend themselves more to growth than others.<br></p>

<p><strong>You don’t want anyone idling</strong>. &nbsp;Everyone should be engaged in productive work at all times. &nbsp;This can be tough to manage because the features you most want people working on might not be specced for a while. &nbsp;If specs aren’t ready, you can also have engineers working on the product discovery process by prototyping and feasibility testing.<br></p>

<p>You want to make sure that <strong>pressing bugs</strong> and other one-off issues are addressed. &nbsp;Often these will not fit neatly under one of your OKRs, but you still need to fix them.<br></p>

<p>You want to be <strong>flexible</strong> enough that if some new but important issue arises you aren’t slavishly following the OKRs. &nbsp;This happens all the time at startups.<br></p>

<p>You want <strong>redundancy</strong> in who knows different areas of the codebase in case an engineer decides to move on.<br></p>

<p>You have to accommodate <strong>vacation, parental leaves, sick days</strong>.<br></p>

<p>You have to recognize that <strong>engineers are not fungible</strong>. &nbsp;They know different parts of the stack, different technologies, different parts of the codebase, and will work on projects at different rates with different quality outputs.<br></p>

<p>You sometimes need to build things to increase company value in some strategic way that might not be directly tied to a user story (say for an investor demo).<br></p>

<p>The things you build can’t just be the product of a stack rank. &nbsp;They need to blend into a <strong>cohesive</strong> product.<br></p>

<p>You may want to bundle certain features for a specific launch.<br></p>

<p>And so on…<br></p>

<p>In short, figuring out who should work on what, and in what order, is a big constraint maximization problem that has no clear best answer. &nbsp;Putting together a simple spreadsheet that weighs the options can be helpful, and I recommend it.  <br></p>

<p>At the end of the day, you want a set of goals that are high impact, cohesive, and the team can rally behind. &nbsp;You want something that can be packaged into a neat effort that you can attach a launch deadline to.  The results should be measurable and something everyone on the team can work towards. <br></p>

<p>But ultimately it’s a judgement call to be made (and defended) by the product decider. &nbsp;Like I said, someone is going to be unhappy.  But it’s your job to get agreement to move the project forward if not agreement on the actual priorities.<br></p>


## Week by Week &#8211; Sprints

<p>Once you have your overall priorities and roadmap set, it’s time to start working on a week by week cadence.<br></p>

<p>What has worked best for my teams in the past is dividing up tasks into weekly sprints. &nbsp;Two-week sprints are ok as well.  Every sprint should be kicked off by a short weekly meeting where each engineer and designer publicly commits to what they are going to get done that week.<br></p>

<p>A few points here:</p>

<ul><li>The things that you want to get done that week should be visible in some public place. &nbsp;It could be a shared spreadsheet, a tool like Asana or Trello or Jira, or just a plain document. &nbsp;Don’t obsess on the format.  What matters is that it’s visible to all.</li><li>It’s important to start the week with everyone publicly saying to the whole team that they are going to get X done. &nbsp;For more senior engineers on the team, they should be coming up themselves with what X is.  For less senior folks, the engineering manager should assign tasks and communicate them &nbsp;&nbsp;Either way it’s important that the engineers themselves commit. This creates <strong>accountability within the team</strong>.</li><li>X should be sized appropriately for a week. &nbsp;This can be tricky, but check with the engineer or designer to make your best guess. &nbsp;I’ve tried to use point systems or other sizing methodologies, but I have never found them to work particularly well. &nbsp;But I’m not against them.  Be pragmatic and don’t get caught up looking for the perfect process.</li><li>X should be scoped and defined so that everyone knows what it actually is.</li></ul>

<p>Here’s an example weekly task list from my last company:<br></p>

![image-2019-04-30-at-4.22.55-pm.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1647493433722/E6_x7XsV2.webp)

<p>As mentioned, the exact format doesn’t much matter &#8211; this one was a google doc that linked out to Asana tasks that had more granular detail on the tasks. &nbsp;We could have done this same type of list in a spreadsheet or in Asana itself, but we liked the simplicity and readability of the Google Doc.<br></p>

<p>After the engineers and designers have made their commitments for the week, I suggest sending them to some larger group outside of the product team. &nbsp;This could be a higher up manager, the sales or marketing team, the CEO, etc.  Sending the weekly plan outside of the product team creates <strong>whole team accountability</strong> and gives visibility as to what is currently being worked on.<br></p>

<p>The thing you send should also <strong>highlight what you got done last week</strong>.<br></p>



## Day by Day &#8211; The Daily Standup

<p>I recommend starting every day except the day of the product team meeting with a short team standup. &nbsp;I’ve seen standups work a number of ways (and not work at all).<br></p>

<p>The point of the standup is to discover issues that could prevent folks from reaching their weekly goal. &nbsp;It’s the main tool an engineering manager and PM has for understanding what is going on, what is blocking the team, etc.<br></p>

<p>The mechanics are simple: get every person on product team in the same room in the morning at a fixed time and have each person say:</p>

<ol><li>What they got done yesterday</li><li>What they are going to get done today</li><li>What they are blocked on or need help with</li><li>And that’s it.</li></ol>

<p>Each person should talk for less than 30 seconds.<br></p>

<p>Good issues to surface:</p>

<ul><li>Engineers blocked on code reviews</li><li>Engineers blocked on design input / not sure how to build something</li><li>Engineers stuck on difficult bugs and needing help</li><li>Engineers being behind on tasks and needing help</li><li>Engineers and dev/ops stuck on deployment cycles and bad merges</li><li>Designers needing input and/or feedback</li><li>Two people working on the same thing by accident</li><li>Two people working in a way likely to cause a conflict</li><li>Bad bugs that have come in during the week and how they are being fixed</li></ul>

<p>Things to look out for:</p>

<ul><li>Do not get into deep technical discussions in standups. &nbsp;Anytime this is happening you should move the discussion to after the standup.</li><li>Do not try to define features or debate priorities during standup. &nbsp;Keep things short.</li></ul>

<p>The standup is the main way that engineering managers and PMs are able to see if the team is on track for the week. &nbsp;If not, it’s an appropriate time to adjust and rebalance tasks, unblock folks, and so on.<br></p>

<p><strong>Standups tend to deteriorate in attendance and quality over time</strong>. &nbsp;I’ve seen this again and again. &nbsp;Engineers start coming in late, the standup gets cancelled a few days when lots of folks are out, the standup goes badly a few times, standup updates start to come in via slack rather than in person.<br></p>

<p>When this happens <strong>it is the job of the team leaders to get it back on track</strong>. &nbsp;The standup deteriorates because engineers would rather not do it. &nbsp;It requires them coming in at a fixed time, it pulls them away from their computers and forces them to talk in front of a group. &nbsp;But it’s important to do because without it, you, as a leader, will not know what’s going on with the team.<br></p>

<p>At my last company I literally resorted to taking attendance. &nbsp;Each engineer had a “standup streak:” the number of consecutive standups they had attended in a row. &nbsp;There were rewards for hitting certain milestones &#8211; ten straight standups got you a free coffee, and so on. &nbsp;It felt like elementary school, but, when we pushed it, it worked.<br></p>

<p>A few folks have asked what I have against Slack standups. &nbsp;I’ll probably write a section on when I think Slack is appropriate (not that often), but I definitely don’t like it for standups because:</p>

<ol><li>Slack updates aren&#8217;t interactive in the same way as in person &#8211; it’s much harder to ask questions quickly</li><li>New slack messages push the standup updates out of the window (i find this to be a general issue with any kind of group slack)</li><li>They tend not to all come at the same time, which causes the standup to actually take longer and cause more distraction</li></ol>


## The Perfect Process

<p>As an aside, I’ve come across many folks in the product world whom I consider overly-dogmatic about product process. &nbsp;People tend to hold something like religious beliefs on how things need to be done.  <br></p>

<p>This is not me. &nbsp;I’ve tried a lot of different systems, tools, and so on, and what I think works best is a pragmatic approach. &nbsp;Do what makes the most sense in the context of your product, team, stage, company, culture and so on.<br></p>

<p>For instance, if you are a very early stage startup with no product, it doesn’t make a lot of sense to base your OKRs on moving customer metrics. &nbsp;You should base your OKRs on getting your <a href="https://blog.leanstack.com/minimum-viable-product-mvp-7e280b0b9418">MVP</a> built as quickly as possible. &nbsp;The Key Results should be MVP features.<br></p>

<p>The specific product planning tools you use rarely matter in my experience. &nbsp;At Google, it was a set of in-house tools.  Externally I have used Asana, spreadsheets, documents, github tasks. &nbsp;The more advanced tools have various bells and whistles, which can enable some advanced workflows.<br></p>

<p>What actually matters is commitment to a process and constant vigilance by the management.  And more than that, what matters is the culture you build.  If the culture favors pragmatism and a commitment to putting the user first, then you will likely be successful no matter what the particulars of the process are.</p>
