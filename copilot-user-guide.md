# Copilot User Guide

**Table of Contents**
- [What is GitHub Copilot?](https://gist.github.com/bthomas2622/dcdbb345dc3d14292bcf12f0b7ad525d#what-is-github-copilot)
- [How do I install Copilot?](https://gist.github.com/bthomas2622/dcdbb345dc3d14292bcf12f0b7ad525d#how-do-i-install-copilot)
- [How do I use Copilot?](https://gist.github.com/bthomas2622/dcdbb345dc3d14292bcf12f0b7ad525d#how-do-i-use-copilot)
- [How do I improve Copilot's suggestions?](https://gist.github.com/bthomas2622/dcdbb345dc3d14292bcf12f0b7ad525d#how-do-i-improve-copilots-suggestions)
- [How do I use Copilot responsibly?](https://gist.github.com/bthomas2622/dcdbb345dc3d14292bcf12f0b7ad525d#how-do-i-uses-copilot-responsibly)

## What is GitHub Copilot?

GitHub Copilot is an AI pair programmer that helps you write code faster and with less work. It draws context from comments and code to suggest individual lines and whole functions instantly.

## How do I install Copilot?

Install Copilot on your chosen IDE. Your GitHub account must possess a [valid Copilot license](https://docs.github.com/en/enterprise-cloud@latest/billing/managing-billing-for-github-copilot/about-billing-for-github-copilot) for use.
- [Visual Studio Code](https://docs.github.com/en/enterprise-cloud@latest/copilot/getting-started-with-github-copilot?tool=vscode)
- [Visual Studio](https://docs.github.com/en/enterprise-cloud@latest/copilot/getting-started-with-github-copilot?tool=visualstudio)
- [JetBrains](https://docs.github.com/en/enterprise-cloud@latest/copilot/getting-started-with-github-copilot?tool=jetbrains)
- [Vim/Neovim](https://docs.github.com/en/enterprise-cloud@latest/copilot/getting-started-with-github-copilot?tool=vimneovim)

## How do I use Copilot?

GitHub Copilot **provides autocomplete-style suggestions** from an AI pair programmer as you code. You can receive suggestions from GitHub Copilot either by starting to write the code you want to use, or by writing a natural language comment describing what you want the code to do ([Demo](https://www.youtube.com/watch?v=TFCYGMLIdOE)). 

Suggestions can be accepted like traditional autocomplete tools by pressing `tab` to accept.

You can configure many aspects of Copilot in your environment. See your [IDE specific Docs](https://docs.github.com/en/enterprise-cloud@latest/copilot/configuring-github-copilot/configuring-github-copilot-in-your-environment) for UX and Hotkeys.

## How do I improve Copilot's suggestions?

### 1. Provide Copilot additional context

Copilot can ***draw context from comments and code from the file you are working in as well as open tabs in the IDE***. The more data you give Copilot the higher chance it's suggestion will be helpful for you.
- GitHub Blog: [How GitHub Copilot is getting better at understanding your code](https://github.blog/2023-05-17-how-github-copilot-is-getting-better-at-understanding-your-code/)

#### Examples of ways to improve context shared with Copilot service:
1. If you are writing unit tests, in additional tabs open the files of the functions you would like to write test cases for.
2. If you would like to write code for a given framework, import that framework at the top of the file before writing code. `const express = require('express');`
3. Copilot can understand natural language, write a comment in plain english (or other verbal languages!) expalining exactly what the code you are about to write is expected to do.
4. Be Specific! For example, if you want GitHub Copilot to retrieve data from an API, specify what type of data you want to retrieve, how to process the data, and what API endpoint you'd like to use.

### 2. Prompt Engineering

*Prompt Engineering* is the practice of giving an AI model specific instructions to produce the results you want. A prompt is a sequence of text or a line of code that can trigger a response from an AI model. 
- GitHub Blog: [How to use GitHub Copilot: Prompts, tips, and use cases](https://github.blog/2023-06-20-how-to-write-better-prompts-for-github-copilot/)

Here are some ways to leverage Prompt Engineering with GitHub Copilot:

#### Provide high-level context followed by more detailed instructions. 

For example summarize what the file is doing in a comment at the top of the file. Then go deeper with more function specific comments and code. 

**`math-utils.js`**
```
# this file contains math utilities that perform complex math functions that can be called from other parts of the application

# the primes() function takes in an array and returns the prime numbers
const primes()

# the factorial() function takes in a positive integer and returns its factorial
const factorial()
```

#### Iterate your prompts

If your initial prompt does not retrieve the desired response, edit your comment with more details and examples, and try again.

Make your ask simple and specific. GitHub Copilot better understands your goal when you break things down.

#### Name your variables and functions with names specific to their purpose

In many cases Copilot can determine what a function should contain just from it's name. Chances are writing code that readable to other humans will also be more readable to Copilot.

### 3. Seek alternative suggestions

For any given input, GitHub Copilot may offer multiple suggestions. You can select which suggestion to use, or reject all suggestions. UX and Hotkeys vary by IDE, see [Docs](https://docs.github.com/en/enterprise-cloud@latest/copilot/getting-started-with-github-copilot#seeing-alternative-suggestions-2).

## How do I use Copilot responsibly?

GitHub Copilot boosts developer productivity, but using it responsibly still requires good developer and DevSecOps practices.
- GitHub Blog: [Responsible AI pair programming with GitHub Copilot](https://github.blog/2023-02-22-responsible-ai-pair-programming-with-github-copilot/)

GitHub Copilot is a pair programmer, an ***additive*** tool for you to write the best code possible. ***GitHub Copilot does not replace sensible Software Development Lifecycle safeguards***. Pair Copilot with these practices to stay in the flow responsibly (not an exhuastive list).

- Manually test code to ensure it's working as intended
- Peer Code Review
- Automated linting
- Automated unit testing
- [Static application security testing (SAST)](https://github.com/features/security/code)
- [Software composition analysis (SCA)](https://github.com/features/security/software-supply-chain)
- Functional, integration, load, and penetration testing

