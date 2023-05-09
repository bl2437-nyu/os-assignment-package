# os-assignment-package

This is my undergraduate senior project.

This is a proposed design of a project-based assignment package for the Operating Systems course, where students will implement a Bitcoin mining simulator in C, making use of concepts from the course material.

## Files included

`srcv4` folder includes all the raw source code that I wrote, with all comments about random things. `srcv4_cleanup` folder contains cleaned-up version of the same code, with deprecated code and useless comments removed. Code for different assignments are all placed in `srcv4/src` or `srcv4_cleanup/src` under different file names, and you will need to either rename the files or modify `makefile` in order to build and run them.

`steps` folder includes template code for students. These templates are simply the source code with part of the code removed for the students to implement. They also come with example assignment instructions for the students, in each respective folder's `readme.md` file.

`tools` folder includes miscellaneous tools that might be helpful for development or modification of the code. They are written in Python, unlike the assignment package itself.

## Requirements

To compile and run code in the assignment package, you need a POSIX-compliant system with `gcc` and `make` installed. It is recommended that Linux virtual machines are installed on students' computers.

Students are assumed to have taken Data Structures and Computer Architecture, and have basic C programming skills. A C warm-up assignment ("part 0") is provided, and students may self-check their C programming skills and seek online resources if needed.

To run programs in the `tools` folder, you need Python 3.

## Quick FAQ

I'll update with more information at a later date. For now, here are some questions you might have:

### Who are you? What is this?

I am Boyan Li, an undergraduate computer science student about to graduate from NYU Shanghai (at the time of writing). This is my senior project.

### Can I read your senior paper?

I'll post it here when it's ready!

### Does it cover every chapter of the OS course?

Currently, no. It currently covers **processes, synchronization, threads, and files**, in this order. It is possible to expand this package to include more chapters.

### Any known issues?

The code currently contains minor bugs that affect the correctness of the blocks and blockchains it produces. However most, if not all, code should still hopefully be operational, and would not affect the parts where OS functionalities are made use of.

The bugs will likely be addressed in a post-release patch.

There are also known limitations in terms of how it perform in-class; these will be addressed in the paper as well as a future version of this FAQ.

### Can I use your work?

For now, no. I will choose a suitable license in the near future, if my grades go well.

### I have things to ask/report, or I want to contribute.

If you have anything you'd like to say, feel free to add an issue.

However, I do not accept contributions for now, to prevent potential issues with grading of my senior project. I will review pull requests some time in the future.

### Will this be available in another language?

Readme, FAQ and assignment prompts will be translated to Simplified Chinese in a post-release patch. The paper might be translated too.

Documentation within the source code files will not be translated.

If you instead meant programming language, I will likely not personally implement a package in another language, but feel free to adapt my idea into whatever language you are teaching with.

### Where can I find your other work?

Unfortunately, every other thing I do on the internet is made using my nickname, which I do not feel comfortable linking to.