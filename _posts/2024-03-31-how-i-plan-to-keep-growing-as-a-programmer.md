---
title: "I Can See Clearly Now (or: How I Plan To Keep Growing as a Programmer) 🌱"
date: 2024-03-31
---

I explained in my previous article how I finally started learning programming again, nearly two decades after the first attempt. What I didn't talk about, however, is the road ahead in this journey, and how I plan to keep learning in the ever-evolving field of software engineering.

Sure, there are many [developer roadmaps](https://roadmap.sh/) out there for anyone who wants to learn Computer Science, but these are often either too generic or too specific for someone to follow as-is. What I want to do here is to lay out a personalized plan that aligns with my learning style, prior knowledge and experience, interests and preferences, and career goals.

## Baby Steps

I believe one cannot know where they're going if they don't know where they are or where they're coming from. So I'll elaborate on [my previous article](https://iamoeg.github.io/2024/02/29/how-i-learned-programming.html) to review my progress.

In a nutshell, the past year has been a meaningful introduction to Computer Science for me: I have gained a good understanding of core programming concepts and paradigms, as well as some basic data structures and algorithms, working mostly with Python, Java, JavaScript, a tiny bit of C, and most recently, Go. I also dived into web development and learned about the different layers of the web stack and how they operate. Additionally, I studied relational databases, and touched on cyber-security and networking basics. In the end, I was able to build a few fully working applications, and make some open source contributions.

Today, I'm pretty confident working with Python and Java, as well as HTML, CSS, JavaScript, and SQL. In terms of specific tools, frameworks and libraries, I was lucky to quickly find a stack that I'm really productive and generally satisfied with:

- Python as a general-purpose language
- Django as my go-to web framework
- HTMX for universal [hypermedia controls](https://hypermedia.systems/hypermedia-reintroduction/) with simple, straight-forward AJAX calls
- AlpineJS for client-side reactivity and UX enhancements
- TailwindCSS for effective UI styling
- PostgresSQL and SQLite for my database needs
- Docker to work in reproducible environments
- Linux as my main OS (Fedora KDE on the desktop, Ubuntu on the server)

What I like most about this stack is that it strikes a pretty good balance between functionality and ease of use: in addition to being very extensible, the high level of [locality of behaviour](https://htmx.org/essays/locality-of-behaviour/) these tools offer means you can quickly become productive with them, without losing too much in terms of what you can do (other than applications with a lot — and I mean _a lot_ — of client-side interactivity).

## Discourse on the Method

Of course, I cannot claim to be a master of any of the technologies above, and there are many other areas and technologies I want to explore further. To be effective, a study plan need to take one's learning style into consideration, so I'll try to summarize mine here.

My general approach to learning is very iterative in nature. Whenever I'm studying something new, I tend to go over the following phases:

1. **Research**: I start by gathering information about the topic I'm interested in from various sources, which I review and filter for quality, consistency, relevance, etc., then study more in depth.
2. **Hypothesis**: After studying the materials, I start forming an initial mental model of the subject that I can reason about, but is still pretty loose and conjectural to some extent.
3. **Testing**: I then need to challenge the model with hands-on practice, and test if my hypotheses are valid, invalid, or need further investigation.
4. **Theory**: After testing my hypotheses, the initial model starts turning into a more formal and systematic representation of how things work and why they work the way they do.

In practice, these steps are far less linear and distinct from each other. In fact, the _theory_ I form at the "end" of the process is never final and continues to evolve as I come across new sources, develop new hypotheses, practice on different problems, etc.

I also find it more manageable to pick up things in increasing levels of difficulty and tend to limit the scope of what I'm studying by learning things in isolation at first. Once I feel confident about my understanding of that limited area, I start integrating my new-found insights with prior knowledge. That way, I can recognize common patterns and make connections between seemingly unrelated topics, while rarely being either completely helpless or bored by any given topic due to an inadequate degree of difficulty.

## Compound Interests

Beyond learning style, I think interests and personal preferences too have considerable impact on one's learning journey. That's especially true in a field like software engineering where you can, to some extent, choose your own adventure. So now that I have learned a few things and built a few projects, I'm able to recognize the aspects that really matter to me: the things I'm interested in, my own programming style, and certain language features.

By building websites and web applications, I've come to realize that web development can — much like the Internet itself — get really messy, really fast… but that doesn't mean I don't like it! In fact, I enjoy working with web technologies very much, and I think it's an excellent entry-point to software engineering in general, since you need fairly broad knowledge to be able to integrate different technologies to build a working solution.

However, I also discovered that I'm interested in much lower-level technologies and applications. I'm indeed curious about language implementations, compilers and interpreters, networking protocols, database internals, etc., in addition to being interested in robotics, electronics, and embedded systems with industrial applications. On the other hand, my artistic side is drawn to signal processing and computer graphics, and I would like to be able to make my own audio effects and synthesizers, implement a shader, among other experiments.

In terms of programming style, I tend to favor simplicity above all else. Experience in other fields has taught me that solutions that are too clever rarely succeed at solving any real problems on the long run, but come at the price of unnecessary complexity that often limits your ability to adapt to changing circumstances or evolving requirements. But keeping things simple requires effort, and I'll admit that telling a sane solution apart from an overly complicated one, or a good from a bad abstraction, isn't always obvious. As a result, I generally approach problems by following a few principles:

- I avoid over-engineering solutions by only solving the problem at hand, not hypothetical ones
- I fight certain abstractions (especially if they entail [multiple layers of class inheritance](https://www.codemag.com/Article/0002081/Some-Pitfalls-of-Inheritance)) until they become absolutely necessary
- I let myself _discover_ emerging abstractions rather than _invent_ ones
- I try to keep my projects' external dependencies to a minimum

As to language features, I have realized that:

- I prefer static typing over dynamic typing: C, Go, Java > Python, JavaScript
- I favor strong typing over weak typing: Python > JavaScript
- I like having functions attached to types, but not necessarily the class-based or prototype-based implementations of that idea: Go > Java, Python > JavaScript
- I appreciate compiled languages over ones that require a runtime environment: C, Go > Java, Python, JavaScript

That being said, I think each language has its strengths and weaknesses, and I'm not overly attached to any technology in particular. They are after all just instruments a programmer needs in their tool-set so they can choose the right tool for the job.

## Where Do We Go Now?

Now that I defined the most important learning factors for me, I can confidently devise a study plan that aligns with both my personal and career objectives. My ultimate goal is to become excellent at what I do as a programmer, regardless of the specific domain I apply my skills to. But that's a high-level target that must be broken down into short, medium, and long term goals.

First, there's fundamental knowledge and a few core technologies that I think are best learned continuously with increasing depth, rather than in a time-constrained manner; in no particular order:

- Data structures and algorithms
- Software architecture and design patterns
- Operating systems
- Database systems
- Networking
- System design
- Compilers and interpreters
- And at least some knowledge of cyber-security, data science, and artificial intelligence

Therefore, I'll be studying these in small chunks over time, focusing on slow but steady progress rather than velocity. This way, I can bring theoretical understanding together with practical applications through real-world experience and projects, thus better cementing my comprehension of these topics.

### In the short term

I would like to complete my career transition into software engineering to gain experience building software at scale and learn from more experienced developers, which means that I need to focus on so-called job-relevant skills for the moment.

Since Java, Python and JavaScript are the most demanded skills for jobs in my area, I will dedicate the next few months to learning the following technologies:

- Java Spring Framework, basically mandatory in most job listings
- TypeScript, along with NodeJS, React, and Angular, because [JavaScript is eating the world](https://www.wired.com/story/javascript-runs-the-world-maybe-literally/)
- Django Rest Framework or Django Ninja, to complement my current stack
- MongoDB and Redis, for non-relational database needs
- And better working proficiency with Linux utilities (coreutils), Docker, and PostgreSQL

Hopefully, I will have moved to a full-time software developer position where I can practice these skills by the time I'm done with this program.

### In the medium term

With more experience under my belt and better understanding of the fundamentals of Computer Science I mentioned earlier, I'll feel more confident to start experimenting with lower-level technologies — at which point I'd like to spend most of my time in the Go and C realms.

The case for Go is compelling for a lot of use-cases thanks to its extensive standard library, and good balance between performance and simplicity, in addition to excellent tooling and seamless developer experience.

C, on the other hand, would enable me to start working on projects targeting constrained environments that require more control over the memory and even better performance than Go, especially for embedded systems, robotics, signal processing, etc.

By the time I reach this level, I will probably need to start learning even more about system administration and infrastructure tools like Terraform, Kubernetes, Ansible and the like, but I'll figure out the details in due time.

### In the long term

Again, with more experience and a better understanding of memory, I'd like to move on to studying Rust. My reasoning is that experience with manual memory management in C (and the inevitable `malloc` bullets to the foot), will help me better understand Rust's complex type system, borrow checker, and other distinctive features.

In the same manner, I'd like to learn a language like Haskell as a proxy to the purely functional paradigm (emphasis on _purely_). The rationale here is that programming paradigms are essentially different ways to represent and solve computing problems, with certain paradigms being better suited for certain classes of problems. Which is why I'd like to gain exposure to functional programming and be able to understand how software is built in pure functions with no side effects, and… what the hell is a monad?!

## Parting Thoughts

Sure, one can never know what the future holds: even the best, most detailed plans get derailed eventually. But my journey is long and my destination far away, and I hope this high-level roadmap will keep me on track, or at least help me maintain the right direction despite the likely detours and rabbit holes along the way.

Thanks for reading!

Sincerely,<br/>
Oussama
