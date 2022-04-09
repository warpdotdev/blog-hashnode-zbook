## Code-first vs. Product-first

<p>There are two kinds of programmers, generally speaking. There are programmers who care more about code, and there are programmers who care more about product. The former &#8211; I’ll call them “code-first” programmers &#8211; are obsessed with how code is architected, what tools, libraries and languages are used, how much test coverage there is &#8211; stuff like that. Code-first programmers are psyched when they check in the perfect abstraction, when they get to use the latest language-feature, when they delete dead code. That is, they love the code they write &#8211; the code is the thing.</p>

<p>The product-first programmer cares about that stuff too, kind of, but only as a means to an end. For product-first programmers, the code is the scaffolding, the support, the steel beams in the building, but not the end product. The end product is, well, the product, not the code, and what matters to them is how well that product actually solves the underlying problem. Does the building stay upright? Do the elevators work? Is the A/C functioning? Do people like being there? Product-first programmers love building and launching and seeing users use what they’ve built. The product is the thing.</p>

<p>Anyone who has worked at a place like Google has met plenty of code-first programmers. They are the teammates who are always refactoring code and nit-picking spelling in your function comments. They are in the micro-kitchen complaining about “spaghetti code,” “technical debt,” and the lack of rigor in other teams’ code review processes. They are probably not fixing bugs or launching features. You can probably tell I’m not a huge fan of the code-first approach.</p>

<p>When I interview programmers I’m always amazed at how many of them seem to think the code-first approach is what I’m looking for. Trying to impress me, they ask: “What’s your unit test coverage like?” Pretty close to zero; this is a startup. “Do you guys use hot new technology X.” Not yet, no, how would that help us build the right thing faster? “Is there a lot of technical debt?” We will have to rewrite everything at some point, but it doesn’t matter right now because we haven’t even figured out the right thing to build.</p>

<p>They have an understandable but fundamental misconception of what programming is all about. Programming is about building products that solve problems for users not about writing beautiful code for its own sake.</p>

<p>And to be clear, this is true at all levels of the stack, whether your users are external customers, third-party developers, or internal consumers of an API. What matters is how the code works, not how the code looks.</p>

<p>Does that mean that I encourage writing bad code? That I don’t care about what technology we use or how the software is architected? Absolutely not &#8211; I care a lot! But I care because I believe if you make the right engineering choices, you will ultimately get to a better product.</p>

<p>I recently had an engineer I’m managing ask me how his code was. I responded by asking two questions back: “Did the feature work well?” and “Did you build it quickly?” “That’s what matters to me,” I said.</p>

<p>And typically, if the answers to those two questions are yes and yes, it’s likely (although not certain) that the code was actually pretty good, because good product usually implies good code. By definition the opposite doesn’t exist by the way &#8211; there is no such thing as good code that produces bad product.</p>

<p>I call this my rule of good code:</p>

<p><strong>If the product doesn’t work well, the code is not good.</strong></p>

<p>In other words, there is no such thing as good code in the abstract; good code can only exist if it’s producing a working product (again, define product loosely here to mean product at any level of the stack).</p>

<p>Over and over I see some engineers producing great product quickly, and when I see the code it’s usually well factored and smartly built. It’s not surprising since it’s hard to quickly build good product in a complicated system with code that is poorly architected or factored or not tested.</p>

<p>Conversely, when I see programmers not launching features quickly, the issue is often overengineering. Or when engineers do launch quickly but the quality is bad, then the issue is usually under-engineering or sloppy code.</p>

<p>There’s no zero sum game here: you should strive for good code, produced quickly, leading to great product. This is what great programmers produce.</p>

<figure class="wp-block-image"><img loading="lazy" width="590" height="320" src="https://i0.wp.com/box5776.temp.domains/~thezbook/wp-content/uploads/2019/04/image-2019-04-26-at-11.57.10-am.png?resize=590%2C320" alt="Image 2019-04-26 at 11.57.10 AM" class="wp-image-17" srcset="https://i0.wp.com/thezbook.com/wp-content/uploads/2019/04/image-2019-04-26-at-11.57.10-am.png?w=590&amp;ssl=1 590w, https://i0.wp.com/thezbook.com/wp-content/uploads/2019/04/image-2019-04-26-at-11.57.10-am.png?resize=300%2C163&amp;ssl=1 300w" sizes="(max-width: 590px) 100vw, 590px" data-recalc-dims="1" /></figure>

<p>The best programmers I know are product-first, but actually have more coding knowledge than the coding-first programmers. They know when to use the chainsaw vs the hand saw vs the chisel. When you need to really get something right (usually the deeper in the stack you are) vs. when you can fake it and just move quickly. When it’s better to just write a normal for-loop rather than a custom iterator. These choices and tradeoffs are what becoming a great programmer is all about, and the ultimate feedback mechanism is how well the product works.</p>