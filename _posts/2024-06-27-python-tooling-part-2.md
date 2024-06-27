---
title: "Python Tooling for the Busy Programmer (Part 2) 🪛"
date: 2024-06-27
---

In the [first article of this two-part series about Python tooling](https://iamoeg.cc/2024/05/31/python-tooling-part-1.html), we went through a few packages that help with setting up a sane development environment with some basic facilities like linting, type-checking, and data validation. Now let's take this setup to the next level by incorporating a few other tools in our workflow for even more productivity, usability, and better code quality.

## A not so short list of Python tools (continued)

Take a deep breath, we're diving in!

![Here we go again...](/assets/img/here-we-go-again-willly-wonka.jpg)<br/>
Source: [memecreator.org](https://www.memecreator.org/static/images/memes/4743162.jpg)

### Effective testing with `pytest`

So you've successfully set up your Python development environment, started working on a new project, and even implemented a handful of features in your program. Up to this point, you could still get away with testing your application manually by running the program, providing the necessary inputs, and checking if it produces the expected outputs. But you realize that this process is prone to errors and you're probably missing a few cases where the program could fail. So, as a good programmer, you started considering ways to test your code more effectively.

Enter [`pytest`](https://docs.pytest.org/), a framework that allows you to write and run tests in an easier, more effective, and less verbose manner than what the [`unittest`](https://docs.python.org/3/library/unittest.html) package from the standard library typically allows. It covers all kinds of testing needs, including unit tests, integration tests, end-to-end tests and functional tests. It's a really robust and full-featured tool with a huge library of plugins to integrate with other packages, like [`coverage`](https://coverage.readthedocs.io/) or [`pytest-cov`](https://pytest-cov.readthedocs.io/en/latest/) to track you test coverage for instance. You could pair it with browser automation tools like [Playwright](https://playwright.dev/python/) or [Selenium](https://www.selenium.dev/) to reliably test a web app. With a good test suite, you can gain at least some assurance about the behavior of your code, but you must be aware that testing does **not** equate to the _absence_ of bugs in your code: it only signals their _presence_. On a side note, if you're interested in this topic, here's a good series of articles about [testing with Python](https://www.bitecode.dev/p/testing-with-python-part-1-the-basics).

### Generating simple data with `faker`

Testing software often requires some data to perform tests with. Of course, the best data you can test your code with is actual data that you could source from a production environment or database (just don't use the real thing, make a copy instead). But this is not always an option, especially in the early stages of development, or if you have some other constraints. In that case, [`faker`](https://faker.readthedocs.io/) helps you auto-generate synthetic data _en masse_, quickly and reliably, so you can use it to bootstrap your database, stress test your system, anonymise data sourced from elsewhere, or use any way you like. It can generate names, emails, credit card details, URLs, phone numbers, addresses, and many other types of data that you will find useful, with many built-in and third-party "providers" (generators), and built-in localization features.

### Generating complex data objects with `factory_boy`

As your project grows in size (or scope), your data will also grow in complexity, and it will become even more difficult to test with. To help with this issue, [`factory_boy`](https://factoryboy.readthedocs.io/) builds upon `faker` by replacing hard to maintain, statically generated data, with factories that generate complex objects dynamically. As a result, you only need to declare test-specific fields for your data objects, and `factory_boy` will take care of the rest by generating the other fields in your classes as needed. It also features built-in support for various ORMs, including Django's and SQLAlchemy's.

### Automate your workflow with `pre-commit`

One of the easiest ways to ensure consistency in your projects is to automate certain checks and fixes like type-checking, linting, and auto-formatting, etc. [`pre-commit`](https://pre-commit.com/) helps you set hooks to perform these actions automatically whenever you commit your changes to your version control system. For example, you could set up hooks for some of the tools we talked about in the last post, like `mypy`, `ruff`, and `bandit`, so that you can fix or at least detect many issues before you add them to your `git` tree or submit your code for review. This way, you or your reviewer can focus on the design and architecture of your changes rather than the more trivial parts. What's great about `pre-commit` is that it's language-agnostic, easily configurable, and highly extensible thanks to its plugin system and the myriad of contributed hooks you can find online for various use-cases.

### Authoring documentation with `mkdocs`

One key aspect of code quality is good documentation. [`mkdocs`](https://www.mkdocs.org/) takes the hassle out of documenting your project by providing you with an easy way to write, style, and even publish your documentation online. I tend to prefer `mkdocs` over something like [`sphinx`](https://www.sphinx-doc.org/) because it's based on Markdown rather than reStructuredText (the syntax of which I find a little too intricate for my taste). Among `mkdocs`' key features are its ability to auto-generate _reference_ documentation from docstrings included in your codebase as well as _ad-hoc_ documentation from simple Markdown files, built-in support for localization, theming, and automatic publishing to a static hosting platform like GitHub Pages. And since we're talking about documentation, I suggest you look into [Diátaxis](https://diataxis.fr/), which is a technical documentation authoring framework that helps with writing quality docs focusing on four documentation types: tutorials, how-to guides, technical reference, and explanation.

### Monitoring your application with `sentry`

Now that your code is fully tested, documented, and ready for production, you should probably consider an observability tool like [`sentry`](https://sentry.io/) to help you track errors, monitor performance, and efficiently diagnose the bugs that arise inevitably when code is pushed to a live environment with real users. With `sentry`, you can track issues in your application, profile performance, set up alerts, replay user sessions, manage releases, and visualise data about your project with custom dashboards and statistics. Additionally, it supports many different languages, frameworks, platforms and technologies. Unlike the other tools in this list, `sentry` is actually a SaaS product, but they offer a generous free tier for solo-projects and have a straight-forward pricing model for teams and larger businesses. Alternatively, you can self-host it on your own infrastructure since it's fully open source.

In any case, you should know that there are many other tools in the observability space, like [PostHog](https://posthog.com/), and [Grafana](https://grafana.com/) for even more advanced needs and use-cases. One recent addition to this space that I find particularly interesting is [`logfire`](https://pydantic.dev/logfire), from the same company behind `pydantic` (which we talked about in the previous article). It's currently still in beta but it seems promising, so I will definitely keep an eye on it.

### Managing Python projects with `hatch`

Now suppose your application grew to a certain size, and you need an environment that's more involved in regard to which versions of Python are supported, how dependencies are managed, recurring scripts, packaging, and perhaps even publishing to a package repository, etc. If that's the case, you should probably consider using a Python project manager like [`hatch`](https://hatch.pypa.io/). It acts as an all-in-one tool to bootstrap new Python projects, define different environments that support different Python versions and dependencies, perform static analysis and testing of your codebase, automate certain tasks via custom scripts, and even streamline versioning and publishing your project to PyPI.

A huge pro for using `hatch` instead of the many available alternatives is that it's standards-based (meaning that it strictly implements relevant PEPs for greater interoperability with the rest of the Python ecosystem), and it's officially supported by the Python Packaging Authority (PyPA). What's more, `hatch` is extensible and features a solid plugin system that integrates with other tools very well. The only downside that I can think of is that it doesn't offer a command _à la_ `pip install <package>` to add new dependencies to a project – so you need to manage those semi-manually in your `pyproject.toml` file (and remember to pin your dependencies to specific versions to avoid unpleasant surprises down the line).

[`rye`](https://rye.astral.sh/) is another Python project manager that offers more or less the same set of features as `hatch`. It was initially developed by [Armin Ronacher](https://lucumr.pocoo.org/) (developer of the Flask web framework, now working at Sentry) who handed the project over to Astral (the team behind `uv`, also covered in the previous post). Like `uv`, it's written in Rust to achieve excellent performance, and it's supposed to play a key part in achieving Astral's stated goal for a fast, unified Python tool-set. The only reason I don't use it as a daily driver is that it's still in experimental phase, as stated in the docs, but it's on my radar.

### Bonus: Scaling software builds with `pants`

Your product is a huge success with a growing feature set, requirements, etc. As a result, you feel the need for a more feature-complete build system to manage your now really large codebase encompassing various projects and packages. [`pants`](https://www.pantsbuild.org/) allows you to perform all the tasks that tend to become somewhat cumbersome in systems that follow a micro-service architecture, including (but not limited to) managing dependencies, testing, build automation, versioning and distribution across services and repositories, etc.

But while it's not required, `pants` really shines in the context of a monorepo [one code repository for all related services, not to be confused with a monolithic _system architecture_] by offering a uniform interface to automate builds for projects that may span different languages like Python, Go, Java, and many others. It's also very performant (the core build engine is written in Rust, and makes extensive use of caching and other optimisations), easily extensible via a Python-based plugin system, and features a simple configuration mechanism.

To be honest, I don't have a lot of experience with `pants` [wait a second... what?!], as I've only used it a few times to integrate Java and Python components for learning purposes. In fact, I discovered it because I was just curious about monorepos and build systems, so I investigated the myriad of tools in this space ([Bazel](https://bazel.build/), [Please](https://please.build/), [Buck](https://buck2.build/)...), and it seemed to be the most straightforward to set up for my needs.

![Pants, or no pants, that is the question...](/assets/img/pants.jpg)<br/>
Source: [quickmeme.com](https://www.quickmeme.com/)

## Conclusion

We went through a lot of tools and packages that can help at all stages of development, but we've only scratched the surface of what Python and its ecosystem offer. Of course, you don't need to use all of them in all of your projects, but I suggest you incorporate them in your workflow as needed. I hope this article helped you at least identify some of the packages that you might need in the future. In the meantime, if you have any tool suggestions for me, let me know  – I'll be happy to try them.

Thanks for reading!

Sincerely,<br/>
Oussama
