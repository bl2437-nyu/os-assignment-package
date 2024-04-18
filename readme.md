# os-assignment-package

This is my undergraduate senior project.

This is a proposed design of a project-based assignment package for the Operating Systems course, where students will implement a Bitcoin mining simulator in C, making use of concepts from the course material.

Read the paper here: [English PDF](/docs/paper.pdf), [English Markdown](/docs/paper.md)

## Files included

`srcv3` and `srcv4` folders includes all the raw source code that I wrote, with all comments about random things. `srcv3` is for the warm-up task, and `srcv4` is for everything else, due to the different data structure and library functions needed. `srcv3_cleanup` and `srcv4_cleanup` folders contains cleaned-up version of the same code, with deprecated code and useless comments removed. Code for different assignments are all placed in `srcv*/src` or `srcv*_cleanup/src` under different file names, and you will need to either rename the files or modify `makefile` in order to build and run them.

`steps` folder includes template code for students. These templates are simply the source code with part of the code removed for the students to implement. They also come with example assignment instructions for the students, in each respective folder's `readme.md` file.

`tools` folder includes miscellaneous tools that might be helpful for development or modification of the code. They are written in Python, unlike the assignment package itself.

## Requirements

To compile and run code in the assignment package, you need a POSIX-compliant system with `gcc` and `make` installed. It is recommended that Linux virtual machines are installed on students' computers.

Students are assumed to have taken Data Structures and Computer Architecture, and have basic C programming skills. A C warm-up assignment ("part 0") is provided, and students may self-check their C programming skills and seek online resources if needed.

To run programs in the `tools` folder, you need Python 3.

## Quick FAQ

### Who are you? What is this?

I am Boyan Li. I graduated from NYU Shanghai with a Bachelor's degree in Computer Science. This is my senior project.

### Can I read your senior paper?

You can read it [here](/docs/paper.pdf)!

### Does it cover every chapter of the OS course?

Currently, no. It currently covers **processes, synchronization, threads, and files**, in this order. It is possible to expand this package to include more chapters.

### Any known issues?

The code currently contains minor bugs that affect the correctness of the blocks and blockchains it produces. However most, if not all, code should still hopefully be operational, and would not affect the parts where OS functionalities are made use of.

There are also known limitations in terms of how it perform in-class; these are addressed in the paper.

### Can I use your work?

For internal use in a higher education institution, you may freely use this assignment package without attribution. It is recommended that you do not include attribution in any material distributed to your students to make it harder for them to find here, but keep a reference for yourself in case you need help.

For every other use, including educational use outside of a higher education institution (eg, on a MOOC platform) and academic or scientific studies, please include an attribution and URL to this repository.

### I have things to ask/report, or I want to contribute.

Feel free to add an issue or pull request. I might not be maintaining this repo, but if I happened to see something coming in my emails, I'll try my best to respond.

### Will this be available in another language?

No, I am no longer maintaining this project.

Feel free to translate anything to your language.

You may also consider porting the assignment package to another programming language to suit your needs. Be aware of differences between languages and operating systems - this assignment package is made for POSIX C.

### Where can I find your other work?

Unfortunately, every other thing I do on the internet is made with my online nickname, which I do not feel comfortable linking to. If you are a recruiter etc that would like to see my personal GitHub account, please leave me a message through the contact information you obtained from my resume.
