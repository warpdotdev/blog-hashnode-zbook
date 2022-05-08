## Introducing Warp: The Terminal for the 21st Century

# Introducing Warp

Today, I’m proud to officially introduce Warp, a from-first-principles reinvention of the terminal to make it work better for developers and teams. As of today, Warp is in public beta and any Mac user can download and use it for free.

We are also excited to announce that we’ve raised some funds to grow Warp ($23M), both from wonderful firms ([GV](https://www.gv.com), [Neo](https://neo.com), [BoxGroup](https://www.boxgroup.com)) and world-class operators like Dylan Field (who led our Series A), Elad Gil, Jeff Weiner, and Marc Benioff.

# Why Reinvent the Terminal?

Walk by any developer’s desk and you are likely to see two apps open: their code editor and their terminal (sometimes the code editor is the terminal!).  

Both are crucial to developer productivity.  The code editor is where developers write code; the terminal is where they do pretty much everything else, from building code to running and deploying it, interacting with source control, configuring their cloud systems, and more.

And yet only one of these two apps – the code editor – has experienced meaningful product improvement over the past 40 years. Compared to using VS Code, using the terminal is like stepping back in time to the 1970s. Only [70% of developers use VSCode](https://insights.stackoverflow.com/survey/2021#section-most-popular-technologies-integrated-development-environment), while 100% use the terminal. So why is the terminal experience still so lackluster?

# Our Product Vision

At Warp, our product vision is to bring the terminal into the present in order to help developers build the future.

‍We are doing this by fixing the two biggest pain points that exist in today’s terminals:

1. Terminals are hard to use
2. They don’t work for teams

These are pain points that I’ve personally experienced again and again in my twenty years as an engineer, and I’m sure readers feel the same.

‍To get good at using a terminal before Warp, users had to do all sorts of complex configuration, master arcane key shortcuts, and memorize abstruse commands. Even then, seemingly simple things like copying a command’s output or positioning the mouse cursor were still difficult.

‍Warp makes input and output easy, and removes the need for most configuration. Input works like a modern text-editor, and output works like a data notebook. Moreover, Warp makes command-entry fast and fun by suggesting commands for commonly used tools and providing built-in workflows that save developers time.

![image_1.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1652031521114/xY6eCQ762.gif align="center")

‍In short, Warp makes the terminal work for the developer, rather than the other way around.

Secondly, up until Warp, terminals have been inherently single-user, local applications.  But as I learned when I was leading engineering on Google Docs – and as Dylan showed with Figma – every productivity application is more powerful when it’s collaborative.  This is true 100% of the time – from Figma to GDocs to Notion to Front – and I’m confident that the terminal is no exception.

Terminal “collaboration” means not just GDocs-style real-time collaboration, but asynchronous collaboration through sharing commands, settings, and history. It means increased knowledge-sharing through wikis and READMEs that run directly in the terminal. It means making the terminal safer and more secure via integrated password-management and audit logging. It means making the terminal a more extensible and customizable platform, with a nice modern ecosystem.

Finally, all of this needs to be built with speed and compatibility in mind – Warp is made in Rust with GPU-accelerated graphics, and works with existing shells like zsh, fish and bash.

# Go Try Warp!

Nine months ago we launched Warp in private beta behind a waitlist.  Since then, thousands of developers have made Warp their daily driver, given us feedback, and allowed us to greatly improve the product.  

Today, we are removing our waitlist and launching our public beta.  We are calling it a “beta” because we know there are still some issues to smooth out, but we are confident that even today the experience is meaningfully better than in other terminals.

If you use a Mac, please give it a shot and let us know how it goes. Otherwise, sign up here to be notified when Warp is ready for your platform.  

Welcome to the future of the terminal.