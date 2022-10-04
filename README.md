# Investing in code reviews for better resarch software

Best Practices for HPC Software Developers webinar series, 12th October, 2022.

## Abstract

Code review is a development practice that improves readability and
maintainability of software projects, in addition to making collaboration
easier and teamwork more effective. Typically, code review is a conversation
between reviewer(s) and the author(s) of the code under review. The code is
dissected and analyzed in order to find areas of improvement according to the
focus of the review. Examples include, but are not limited to, readability,
security or performance improvements. Despite code review being an effective
tool for improving software quality, it is still not a standard practice within
the scientific software development process. The webinar will detail the
benefits that code review can bring to scientific software developers,
particularly improvements in software quality, improved teamwork and knowledge
transfer. The presenters will highlight common difficulties faced by
researchers to set up, perform and maintain frequent code reviews, and they
will discuss several approaches and good practices to mitigate these
difficulties. The presenters will also describe common tools that make code
reviews easier and give examples of how to use them effectively, while
explaining a typical code development cycle with continuous integration and
automatic code checks.

## Contributing

The slide show is written in markdown, to be turned into a HTML slideshow
(reveal.js) with pandoc.

Start by cloning this repository

```
git clone git@github.com:tlestang/HPCBC-code-review-12102022.git
```

The slideshow is contained in directory `slides`:

```
slides/
    slides.md
	img/
```

The slides are generated and deployed at

[HPCBC-code-review-12102022/slides.html](https://tlestang.github.io/HPCBC-code-review-12102022/slides.html)

automatically each time new commits are pushed to the `main` branch.

To build the slides locally, you'll need
[cmake](https://cmake.org/download/) (3.17+) and
[pandoc](https://pandoc.org/installing.html) (2.10+). In the repo's
root directory:

```
mkdir build && cd build
cmake ../slides
make install
```

Generated HTML slides are located in the `generated/` within the build
directory.

In order to make the sources for this presentations easy to work with, please
follow the following style rules:

- Lines are wrapped at 79 characters.
- Section titles are surrounded by one blank line.
- Lists are surrounded by one blank line.
