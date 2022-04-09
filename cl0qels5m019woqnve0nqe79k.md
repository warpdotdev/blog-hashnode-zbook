## Coding

## How to make a change to a shared codebase

<p>When multiple developers are working on the same codebase, it’s important that everyone follow the same procedure for making changes. &nbsp;This is software engineering 101, but the details matter and new engineers don’t always come out of school knowing how to do this.<br></p>

<p>Here’s how I have done it with my teams in the past. &nbsp;<br></p>

<p>Let’s assume for simplicity’s sake that we have the following set up (if you don’t have something like this, then start by getting it in place):</p>

- Your code is stored in some shared repo, say Github.
- Everyone is using git or something similar for version control.
- There is a continuous build, test and deployment system.
- There are at least three environments code can run in: local (not committed), staging (not real users, but hosted in a prod-like environment), and production.
- The goal is to write and test code locally, test it in staging with real-ish data and services and other pending changes, and push it to production as quickly as possible and with as few bugs as possible.

<p>How to make a change? &nbsp;Bear with me if this seems basic &#8211; i’ll add some color below.</p>

1. **Create a local branch** off whatever your team’s “head” branch is. &nbsp;Usually this is <em>develop</em> if you are using <a href="https://datasift.github.io/gitflow/IntroducingGitFlow.html">gitflow</a>, but it could also be <em>master</em> or some other branch. &nbsp;It’s where the up to date code lives and features and bug fixes start from.
2. Make a **small, incremental change**, test it locally, push it to staging and test there.
3. **Review your own code** before sending it to someone else to review.
4. **Assign a code reviewer** and ask them for a code review.
5. **Respond to or acknowledge every code review comment** from the reviewer and ask them to look again until they approve.
6. **Deploy your code to production** and merge the branch into master.
7. Repeat.

<p>That’s the basic procedure. &nbsp;Here are the rules on how to do this workflow well&#8230;</p>

## Writing Code

### Incremental changes

Changes should be as small as possible while still doing something meaningful; small, incremental changes are
- Easier to review: it’s easier for a reviewer to grok a small change and also less of an interrupt so you are likely to get a review more quickly
- Easier to test: smaller changes mean less surface area for testing and more confidence that they work
- Less likely to have merge conflicts when you sync locally
- Less likely to cause merge conflicts for others when you submit
- Easier to roll back
- Pretty much better in every respect

But don’t make the change so small that the overhead of the review and commit would make it make sense for the change to be bigger. **Be pragmatic.**

### Feature-flags
Use feature-flags or some similar mechanism to check-in incomplete code

<ul><li>The most common reason I see big changes is because engineers don’t want to check in half-working code. &nbsp;Feature-flags are the solution here.</li><li>It’s fine for code that is not fully functional to be committed so long as it is not executed.</li><li>Feature flags also have other important uses for staged rollouts and canarying, so it’s good to get them in place right from the start.</li></ul>


### Thoroughly test your own code

<ul><li>If you’re fortunate enough to have support in the form of a QA team or a group of manual testers, that’s great, but ultimately <strong>you are responsible for the quality of what you launch</strong>.</li></ul>


### Get code reviewed early on

<ul><li><strong>The beginning of a feature is the most important time to get a code review</strong>. &nbsp;It is preferable to make an initial commit on a new feature as early as possible because most of the important design decisions are made at the beginning of implementing it. &nbsp;</li><li>A common mistake I see in feature development is not getting the code reviewed until way too much of it has been written, at which point it becomes much more painful to adjust in case a reviewer requests a big design change.</li><li>I’ve seen a lot of sub-par code checked in because the initial change was too big and the author didn’t want to redo it and the code reviewer didn’t want to push the author because of the amount of time it would take. &nbsp;That’s a bad outcome.</li></ul>

### Don’t group unrelated changes in a single review

<ul><li>It makes the change harder for a reviewer to understand.</li><li>It makes it harder to selectively roll back if one part of it causes an issue but the other part is fine.</li><li>But again, be pragmatic. &nbsp;You don’t need to send five distinct code reviews if that would end up taking everyone a lot more time.</li></ul>

### Code should make it all the way to head on every review

<ul><li>Don’t have code incrementally reviewed on a single branch as you build out a feature and then submit that one branch once the feature is fully built</li><li>This leads to committing one big change at the end, which, for reasons stated above, is bad</li><li>Use feature-flags to submit incomplete code &#8211; that way you can separate committing and pushing the code from enabling the code.</li></ul>

### Keep working while your code is being reviewed

<ul><li>The technique I recommend is &#8220;branching off of your current branch&#8221; to keep going. </li><li>E.g. if you are having &#8220;feature_branch&#8221; reviewed, then you should locally do &#8220;git checkout -b feature_branch_2&#8221; from feature_branch and keep working. </li><li>As you make changes for the initial review in &#8220;feature_branch&#8221; you merge them into feature_branch_2 so it picks them up. </li><li>Finally, when you submit feature_branch, you merge master into feature_branch_2 and it becomes the next thing you have reviewed.</li></ul>

### Do not share feature branches

<ul><li>Under no circumstances should engineers share feature branches. &nbsp;By “sharing”, I mean if two or more engineers are working on a single feature off of a non-head branch. &nbsp;</li><li>There are many reasons this is a bad idea, but the primary one is that this encourages the submission of very large changes, and for the reasons listed above, large changes are bad.</li><li>It also makes it hard for other engineers on the team to review code early enough to catch errors.</li></ul>

### Use a linter for enforcing style

<ul><li>Using a linter like <a href="https://eslint.org/">eslint</a> or <a href="https://prettier.io/">prettier</a> that enforces a particular code style saves a lot of time commenting on style issues in code reviews and also keeps the code consistent.</li><li>I’ve seen teams put in presubmit checks that verify the code style is followed. &nbsp;I don’t recommend this because it’s likely to annoy anyone external to your team who is trying to make a small fix in your codebase and doesn’t have your linter configured. &nbsp;Either make it so the linting is automatic or don’t rigorously enforce at check in time.  Someone will fix it on the next PR.</li></ul>

## Code reviews

Code reviews are <em>the</em> most important quality check there is in writing new code. &nbsp;If there is one quality control practice I would prioritize above all others it’s a culture of good code reviewing.

### For the author
- Always merge master into your feature branch before starting the review process &#8211; otherwise your diff might show spurious changes and you could end up with a change that needs merge conflict resolution after the review
- <strong>Review your own code before you ask someone else to review it! &nbsp;</strong>Make sure what you present to the code reviewer doesn’t have changes you know you should make.
- <strong>Do not expect code reviewers to find bugs!</strong> &nbsp;They sometimes will, but that is not their job.
- Assign the review to the person who knows the area of code you are working on best, not the person who does the easiest reviews. &nbsp;But try to spread your reviews around if you can.
- New team members should act as “secondary” reviewers on a bunch of code reviews before reviewing code on their own. &nbsp;
- If you are really trying to scale a codebase, you can introduce a concept of “readability;” any engineer who has “readability” in a programming language is allowed to approve a change on his or her own. &nbsp;Otherwise, they need another reviewer to approve. Google has this process in place, but they also have a huge codebase they are trying to scale.  I would not recommend this for a startup.
- Continue working by branching off of your feature branch while you are waiting. &nbsp;This is a powerful way not to get blocked.  See the technique of branching off a branch above.
- If you are blocked on a review, you should be aggressive in pinging the reviewer, and, if that doesn’t work, a manager. &nbsp;<strong>Fast code reviewing is a key part of a healthy team and everyone should feel responsible for reviewing code quickly. &nbsp;</strong>Speed of review is inversely correlated with the size of the change, so if you want your changes reviewed quickly, keep them small.
- When a review comes back, address every comment, even if just acknowledging that you made the suggested change.
- Test your code again after you have made the suggested changes! &nbsp;Blindly commiting the reviewer’s suggested change is a common source of bugs and build breaks.
- Code reviews from more senior engineers are how you become a better coder &#8211; remember that. &nbsp;Don’t get defensive when an engineer requests changes.</li></ul></li>

### For the reviewer
- <strong>Treat code reviews as high priority.</strong> &nbsp;If you can’t immediately direct your attention to the review, you should let the author know when you expect to get to it. &nbsp;I don’t think any review should sit for more than a couple hours unaddressed.
- <strong>Focus on design issues first and foremost. </strong>&nbsp;The most impactful reviews ask a few key questions about design issues that are likely to cause problems down the line if not addressed early on.
- Keep the tone focused on learning and improvement and not critical. &nbsp;Engineers are sensitive about criticism and the more you focus on making the code better and not pointing out what someone has done wrong, the better &#8211; i usually frame my feedback as suggestions.

Example good feedback:
- “It looks like this might run in n^2 time &#8211; is there a way to make it linear?”
“I think this is making a network call within a tight loop. &nbsp;Maybe add a bulk api on the server side so you can do the work in one call?”
“I’d think about putting all of these methods into their own class and memoizing the calls if you can”

And not so good feedback:
- “Style guide for JS Doc calls for two newlines between top level file comments.”
- “NPE”
- “I didn’t understand how this worked but if you’re sure it produces the right results, then ok.”

## Presubmit checks

<ul><li>A “presubmit” check is a trigger that automatically runs <em>before</em> your code gets merged and deployed.</li><li>Examples of presubmit checks are scripts that check the formatting and linting of code, ones that check the code has been reviewed, etc.</li><li>The most valuable presubmit routine you can have is one that takes the code you are about to merge, integrates it into the production “head” in another sandbox environment, and builds and runs all of your tests against it. &nbsp;The important thing is that this happens <em>before</em> the code is merged, so you avoid breaking the build and tests.</li><li>See this awesome <a href="https://blog.bubble.is/look-ma-no-master-decentralized-integration-3706d43d5c86">post</a> by Josh Haas on how they implement this at Bubble.</li></ul>

## After submitting and pushing the code

<ul><li>Code is almost never “done.” &nbsp;There are always bugs that arise, which brings me to my next point&#8230;</li><li><strong>FIX YOUR BUGS. </strong>If you push a bug, fix it. If you create a bug somewhere else in the product because of your change, fix it or roll back your change. &nbsp;Great engineers are always fixing not only their own bugs but other bugs they find in the product.</li></ul>

<p><strong>IF YOU BREAK A BUILD, ROLL BACK.</strong>  This depends somewhat on the nature of the break, but a broken build slows everyone down and your default should be to roll back your change rather than trying to roll forward with a fix.</p>
