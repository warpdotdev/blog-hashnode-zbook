## Multiply by 𝝅

<p>There’s no question that’s harder to answer as an engineer, eng manager, or PM, than “when is this project going to launch?” Honestly, the question is hard to answer because it’s hard to actually know. And generally, the bigger the project, the larger the uncertainty. This is doubly unsatisfying because big features are most anticipated and folks are most disappointed when they run late, as they usually do.</p>

<p>I led a project at Google that was over a year late. Granted, it was a big project &#8211; a rewrite of Google Sheets. But I was off by a whole year, which seems crazy in retrospect. How did this happen?</p>

<p>I made a few mistakes right at the outset.</p>

<p>I, like most engineers, have a bias towards optimism in my coding ability. I thought my and my team’s code wasn’t going to have as many bugs as it ended up having. I misjudged the number of tasks we had to complete. I underestimated the number of external dependencies we had. And so on&#8230; it’s just a lot easier to think of what you need to do if the project goes perfectly than if things go wrong.</p>

<p>I also over-promised to get buy-in. I’m typically pretty reserved in making promises, but for big projects there is a built-in incentive to say they are going to go as well as possible and under-represent the risks. If you give too conservative of a timeline you run the risk of not getting the go-ahead from decision makers &#8211; no one wants to fund a 4-year software project (for good reason).</p>

<p>I also just flat out didn’t think through how much work was really going to be involved.</p>

<p>During the first internship I ever had &#8211; at a dot-com-bubble company that’s long since gone &#8211; the CTO spoke to this question. He said “Here’s how I estimate: I take whatever time the engineer says and multiply by 𝝅. Why 𝝅? Because it’s more fun than 3, so why not?” I thought it was really weird at the time.</p>

<p>Almost 20 years later, the multiply by 𝝅 rule seems pretty accurate. I’ve seen very, very few projects or large features launch on time, but scores that have taken over 𝝅x as long as they were supposed to.</p>

<p>Projects tend to start slow. When we first started on the Sheets rewrite we wanted to do everything The Right WayTM. All our classes were perfect. We agonized over code reviews. We were determined not to make the mistakes of the prior version. Of course, all of this “perfection” came at a cost of time. But at the beginning the time pressure wasn’t intense, so it seemed fine.</p>

<p>As we got further along, we started to lose the luxury of time. Stuff came up that we couldn’t or didn’t foresee. A year into the project we realized the performance of our new architecture was actually way worse than expected, worse than the version we were replacing. Oops.</p>

<p>We had to stop all forward progress and spend the next four months working on speeding up the app (thankfully we were able to). It would have been hard to plan for this particular issue, but I should have seen the risk of something like this happening.</p>

<p>The specifics vary, but the general pattern is the same &#8211; shit happens and your project gets delayed. And once it’s delayed, there’s usually no way to get it back on schedule. The instinct around adding more engineers usually ends up in Mythical Man Month-land slowing things down further. The best thing is often to just start cutting features. No one really likes this though.</p>

<p>How can you minimize the risk in the first place? Ever since the sheets rewrite, I always start by taking the project’s big tasks and breaking them into smaller ones. However, the idea is not that you get to a more accurate estimate of the big task by dividing it into smaller ones and adding them up.</p>

<p>The idea is more that by breaking up the big tasks you can get a better sense of the true surface area of your feature or project &#8211; it’s a reality check.</p>

<p>For our Sheets rewrite I would have ended up with a huge list of features, functions, and so on &#8211; everything that goes into a spreadsheet app from the UI of formula editing, to pivot tables, to sorting, and so on. I couldn’t have really said that writing pivot tables was going to take X weeks and charts Y months with any accuracy. But by looking at those features I could have realized at some subconscious level how big the effort really was. I should have been more scared.</p>

<p>As an aside, “divide and add up” is not a good estimation method. The problem is that most of the time in software development isn’t spent writing code for features. It’s spent in integration, debugging, testing, handling changing requirements and so on.</p>

<p>There’s an 80/20 rule at play here, and goes against the instincts of the estimator &#8211; the 80% is spent after the initial code is written, but it’s very hard to list out how this time will be spent beforehand. When you divide and add up you leave out those hard-to-name tasks and end up with an underestimate.</p>


## Deadlines

<p>So what’s the actual way to deliver on time? Unfortunately, the best thing I’ve seen is to set a deadline.</p>

<p>I say “unfortunately” because from the developer’s perspective, deadlines suck. Developers tend to think things “take as long as they take” and adding on an arbitrary date doesn’t change the fact that the software takes a certain amount of time to write and debug. It just adds pressure. It creates a death march mentality.</p>

<p>I totally get this perspective.</p>

<p>However, setting a launch deadline and orienting the team around it has all sorts of benefits that actually do move projects along faster.</p>

<p>The proper way to set a deadline is to establish the “when” and leave a little bit of flexibility for the engineering team around the “what;” meaning you say that product/feature X needs to launch by day Y, but there is some flexibility around what exactly will launch depending on what is feasible. But the goals should be aggressive.</p>

<p>Once you have a deadline, time becomes a limited resource; you become more conscious of wasting it.</p>

<p>Deadlines let you backtime; if the deadline is date X, then you know you need to have rolled out to internal testers by X &#8211; 4 weeks, and that means the code needs to be complete by X &#8211; 8 weeks, and so on, which means your first feature needs to be done in 2 weeks. Better start coding!</p>

<p>Deadlines create competitive motivation. You don’t want to be the sole engineer on the team who makes the project ship late.</p>

<p>Immovable deadlines really motivate. If your deadline is tied to a public facing event (say Google IO or the launch of GDPR), then you most likely will have something ready to ship.</p>

<p>The issue, of course, is that deadlines can seem arbitrary and if you use them too often it ends up feeling to engineers like a never ending emergency.</p>

<p>The best way to overcome this is to:</p>

<ul><li>Not always be in deadline mode &#8211; sometimes there needs to be space for exploration, design, cleanup etc.</li><li>Save deadlines for the most important features</li><li>Try to pick deadlines that have a plausible business rationale (e.g. an external conference or a competitor releasing a product)</li><li>Get the leaders on the team totally bought in on the deadline and make it a fun cultural thing (print tee shirts, and so on)</li><li>Make the deadline as realistic as you can without sandbagging</li></ul>

<p>In retrospect, I wish our Sheets rewrite had a deadline. I bet we could have gotten it done at least six months sooner. There would have still been unforeseen issues, feature cutting, and so on, but we would have approached the whole project with a greater sense of urgency and clearer prioritization from the get-go.</p>

<p>Also, be careful of rewrites in general! That’s a subject for another post though…</p>