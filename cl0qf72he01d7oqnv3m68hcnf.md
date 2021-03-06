## The Biggest Mistake I See Engineers Make

<p>Throughout my career, the biggest mistake I see engineers make is doing too much work on their own before looping in others.&nbsp;&nbsp;</p>

<p>I’ve experienced this mistake as both an IC and a manager. As an IC, it’s a mistake I made many, many times early in my own career. As a manager, I made the mistake of not recognizing and fixing it in the engineers I’ve managed.&nbsp;&nbsp;</p>

<p>Correcting this habit is the most common feedback I now give, so I thought it might be good to write out how it happens and how it can be avoided.</p>

<p>The typical scenario goes something like this:</p>

<ol><li>An engineer takes on a relatively big / important project, usually building a feature or piece of infrastructure.&nbsp; The bigger the project, the likelier the situation to follow this pattern.</li><li>The engineer goes off on their own and starts by trying to figure out how to build the thing.&nbsp; Often this is verbally framed as “exploratory work”, “designing”, or something else without a concrete deliverable or timetable.</li><li>Throughout this initial period there are standup updates of the form “I’m exploring X, or working through problem Y, but should have something for others to take a look at soon”</li><li>Finally, after several weeks, the engineer shares an update, and one (or many) of the following bad things transpire:&nbsp;<ol><li>They have started building the thing and are about to send out a really big initial PR for it (oy!).&nbsp; For reasons I talk about <a href="https://thezbook.com/coding/#small-changes">here</a>, you always want to send the smallest PRs you can, and generally for big features you should start with a design or prototype, not a PR.</li><li>They have actually been solving the wrong problem because the feature wasn’t well specified (which is normal, and speccing a feature out more completely is often part of building it). &nbsp; E.g. they assumed that their feature would work way X, but the rest of the team was thinking it would be Y, so the design or code isn’t right.</li><li>They have been trying to figure out the solution to some very specific part of the problem, which actually might not be important at all because we could easily trim back the product requirements to avoid it.&nbsp; (E.g. they have been devising a locking solution for something that doesn’t even require concurrency).</li><li>They have designed a very involved, complex, overall solution which if they had got feedback on earlier we might have redirected to a totally different spot.&nbsp; E.g. the solution has multiple new microservices where there could have just been a library.</li></ol></li></ol>

<p>These outcomes are all bad for the same two reasons:</p>

<ol><li>There was a huge cost in time without a lot of forward progress on the project.</li><li>We end up in a position of dealing with the <a href="https://thedecisionlab.com/biases/the-sunk-cost-fallacy/">Sunk Cost Fallacy</a> where it hurts to abandon the work already done in order to get back on track – if we aren’t careful, we’ll end up shipping the wrong thing because we didn’t want to swallow the sunk cost.</li></ol>

***Why does this happen?***

<p>For early career engineers, it often happens because they lack practice working on teams.&nbsp; They train in school environments where they do classroom projects on their own, or work on long-term intern projects in a silo.&nbsp; They are used to having to figure it all out up front, submit it for review, and then get some sort of result, like a grade or return offer.</p>

<p>For more senior engineers, it can happen because they like to work on their own and may be overconfident in finding solutions.&nbsp; It can also happen if the team culture is toxic and engineers fear getting criticism early in the design process.</p>

<p>Building software on a team shouldn’t work this way though.&nbsp; When you work on a team, you shouldn’t be in competition with other schoolmates or interns or teammates – you are working cooperatively to ship the best possible product, as quickly as possible.&nbsp; And there’s a huge advantage in leveraging the team’s collective wisdom to build better and faster.&nbsp;&nbsp;</p>

<p>Early career engineers don’t always know this – they need to be taught it.&nbsp; Senior engineers can be overconfident and need to be reminded of it.&nbsp; And as a manager, you need to be on the lookout for this flawed approach in order to keep your team productive.</p>

<p><strong>To sum up, just as a product is likely to be best if it is developed iteratively with users, the work of an engineer will be best if developed iteratively with the product team.</strong></p>

<p>Concretely, if you’re an engineering manager, this means the following:</p>

<ol><li>Always encourage engineers to show their work as quickly as possible – an engineer on a project should never go more than a week without showing something, and usually it should be more like a day.&nbsp;&nbsp;</li><li>The thing they show could be a design doc, a PRD, a prototype – anything that puts the team in a position to give meaningful feedback as early in the development process as possible.&nbsp;</li><li>If the engineer is unclear on a first deliverable, help them decide on what (e.g. a design doc) and by when (e.g. in two days).&nbsp; And so on for the next deliverables.</li><li>Encourage engineers to get something end to end launched internally as quickly as possible.&nbsp; In other words, rather than developing the feature in a waterfall fashion, where the engineer does the complete data model, followed by the complete controller logic, followed by the complete view, encourage doing just a partial data model, controller, view that works end to end for some small part of the feature.&nbsp; This will give everyone a better sense of the feature from a user’s perspective and will also be the easiest way to see how the pieces of code fit together.</li><li>Development should always be done behind feature flags so that features can be checked in incrementally.</li><li>Demo, demo, demo – continue to demo the feature as it gets fleshed out.</li><li>Separately, you should encourage everyone on the team to give constructive feedback, and be on the lookout for any feedback that is overly negative or toxic, since that discourages developers from working iteratively.</li></ol>

<p>Hope this is helpful!!</p>
