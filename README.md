# The Buried Lede of Data Journalism and Learning to Code

Inspired by MIT's ["Missing Semester of Your CS Education"](https://missing.csail.mit.edu/) (related HN thread / tweet thread), but tailored to folks who aren't learning computer science as a career or degree program – in other words, people who want to learn programming to be better at whatever their current job or passion.

## The pitch

This guide aims to teach a broad set of computing and data concepts and skills, immediately useful for "getting things done", to an audience of every and any technical background and comfort.

Whether you just need to get things done, or you aspire to new career and educational paths (e.g. "learn to code"), this guide also aims to build a foundation of technical confidence and happiness that hopefully greatly accelerates and expands your continued studies.


## Main goals

- Minimal viable education: teach concepts and skills in order of immediate usefulness and ease of understanding.
    - for example, if you stop at Chapter 2, all the things I cover in it (especially keyboard shortcuts!) will be useful to you in everyday computing, even if you never pick up this guide again.
- Accessible to non-programmers and hopefully, tech novices in general. 
- Cover skills and tools equally useful to non-programmers, CS students, and STEM professionals in general (e.g. researchers and data scientists)
- Flexible technical requirements for the most common denominator, to minimize the work needed to jump in and learn
    - assume and use system defaults
    - minimize external dependencies and software
        - but don't be too hardcore – it's beyond the scope of this guide to train users on vim
       - when third-party software is needed, use the most popular variation, e.g. VS Code instead of Sublime Text (even though I'm a diehard )
    - for now, I'm focusing on writing for MacOS before translating it to Win10

- Not "real" programming/computer science. 
    - Shell scripting – like Excel formulas – *is* programming, of course. But you can do very useful and advanced things without actually grokking variables, functions, and control flow. 
    - Definitely not concepts like algorithmic efficiency, parallel processing, or memory management.
    - For the purposes of this guide, we don't get into anything like Python or JavaScript. I do cover **R**, but less as a programming environment and more as a high-level toolbox for visualization


### Secondary goals

- Build skills needed to be a better learner (e.g. how to debug and Google search)
- Cover real-world data collection and wrangling
    - How to find and get it
    - Its (many many) complications
    - How politics affect our data and vice versa
- Show the creative side of scripting and data
    - data viz
    - art projects!
- Structure content so it's easily translatable to vidcast tutorials

## Syllabus (brainstorm in progress)

Random brainsplurge, covering whatever big ideas (what is data) and pedantic minutiae (how many bytes does a PDF scan have) I could brainstorm in 15 minutes.

### Unit 1: The Everyday Setup

- The setup
    - Download:
        - Chrome or Firefox
        - VS Code
        - RStudio (for much later)
        - DB Browser
    - Create accounts:
        - Google (for Sheets)
        - Github 

- Operating system fundamentals
    - Keyboard shortcuts
        - Clipboard stuff Cmd-A Cmd-C Cmd-V
        - Tab
        - Context/app switching
        - Screenshot to clipboard Cmd-Shift-4
        - Jump to filepath Cmd-Shift-tilde
    - Navigating your file system
        - Enable: show files as list
        - Sorting
        - Naming conventions
        - Making new folders
        - General organization ideas

- What are files
    - enable Show file extensions
    - Open As...
    - what is a PDF and why is a PDF
    - demystifying bytes and binary
        - how many bytes for 500-words of text
        - bytes per video minute
        - bytes for a jpg vs a png vs a tiff vs a gif
            - what is lossless
        - how to tell a pdf is "text-based" or a scan based on bytecount alone

- Browser smarts and Google-Fu
    - Google
        - syntax operators
            - site:
            - filetype:
            - minus
            - literal
            - order of operations
        - How to search for errors
            - how to read ugly error messages
            - how to generalize error messages to find relevant search results
    - Browser tips
        - Configuration
            - Always download a file (except for media)
            - know the download directory path
            - using History and avoiding tab-overload
            - Show warning before quitting with Cmd-Q (Chrome)
            - Creating multiple browser users/profiles for multiple tasks
            - Cool plugins
                - Close all tabs but this one
                - Screencapture

        - Keyboard shortcuts
            - New window vs new tab
            - Window cycling (cmd-tilde)
            - Command-L to edit browser bar
            - Space/Shift-Space for page up/down
            - Cmd-Shift-T to open last closed tab
        - Incognito mode (esp. for non-personalized search)
        - The importance of URLs
            - what are query strings and how to tweak them for fun
            - what a URL tells you about an organization, and vice versa
                - [How a High Schooler Scooped Everyone on the Iowa Poll](https://www.nytimes.com/2020/01/10/business/iowa-poll-student-scoop.html)
        - Basic dev tools
            - How to view source
            - Finding URLs
            - the network panel
                - copy as cURL (?)
            - Disabling Javascript
            

### Unit 2: The Joy of Plaintext

Most layfolk don't understand what text is, especially text apart from a Word document. But data and code IS text. Learning to think in text, and to do as much as possible in text, is they key to truly understanding data and programming.


- Plaintext and data
    - brief intro to VS Code
        - syntax highlighting
            - sample HTML page (example.com)
            - JSON file
        - .docx vs .txt
        - intro to markdown / wean yourself off .docx / what is "syntax" in general

    - Text is just data
        - opening a Excel-made CSV in VS Code
        -     
    - Intro to plaintext data formats
        - CSV
        - JSON
        - making a CSV from scratch
            - opening it in excel
            - excel Save As...
            - Delimiters and quoting (i.e. complex CSV parsing)
        - JSON from an API
    - What is code
        - code is just text
        - making HTML from scratch
        - a Python script
        - the Python interpreter
    - Unicode and text-encoding (very briefly)

- Regular expressions
    - thinking in patterns
    - what's a syntax
        - understanding escape characters
    - Using regex in VS Code:
        - enabling regex search 
    - basics
        - dot-char
        - character classes
        - one-or-more
        - either-or
    - grouping and named groups
    - more regex in VS Code
        - find and replace on steroids
        - global search with patterns
    - real-world useful regex patterns
        - converting between date formats
        - extracting parts of addresses and names
        - quick-and-dirty data cleaning for Excel, e.g. removing non-numerical symbols in number fields

- Advanced text editors
    - Project sidebar
    - Customization
    - Grepping and file search
    - Syntax-specific snippets/tab completion
        - Emmet for HTML (already built-in for VS Code)
    - Plugin ecosystem


### Unit 3: The Command-Line Life

It's possible to be great at data and programming without knowing jack about the shell and the command-line. But such a path is pointlessly dumb and painful. Grokking the Unix philosophy – do one thing and one thing well – and the practice of piping data (i.e. text) between simple utilities, is so useful you may not even need to do "real" programming. And if you do need real programming, the command-line only makes you much much better at learning and using it.


- Everyday Command-Line Basics
    - Terminal.app
    - Keyboard as destiny
        - Tab to autocomplete
        - up/down for history
    - Built-in useful CLI utils
        - curl
        - whois
        - VS Code + Shell
            - using `code` to open from the command line
        - MacOS specific utilities
            - open
            - pbcopy and pbpaste
            - screenshot
            - say
            - brew

    - Primer on shell syntax
        - whitespace is important
        - backslash
        - quoting stuff
        - flags and arguments

    - Awesome 3rd-party CLI
        - how to brew install (hopefully)
        - youtube-dl 
            - output different title
            - get audio only
            - get subtitles
        - pandoc
        - pdftotext via poppler/xpdf
        - wget
        - ffmpeg / convert
        - giffify
        - stylecloud https://github.com/minimaxir/stylecloud
        - twarc (twitter auth stuff)

- Command-Line Mastery
    - Keyboard shortcuts
        - TAB TO AUTOCOMPLETE DAMMIT
        - Ctrl-A/Ctrl-E
        - Ctrl-C
    - Filesystem navigation
        - pwd and ls
        - cd
        - home directory and other aliases
        - wildcards
        - mv and cp
        - mkdir
    - general utils
        - history
        - man
        - cat
        - head/tail
        - wc

- The Unix Way
    - Be good at one thing and one thing only
        - why unix utils seem so basic
        - as a general design and programming philosophy
    - common nix utils
        - grep
    - pipe operator
        - pipe pipe pipe
        - cat | grep all the things
    - file redirection
        - the dangers of unix


### Unit 4: Real World Scripting 

How to tie the minutiae you've learned to what you probably imagined "real" programming to be. A light introduction to the concept of best practices in software engineering.


- Data wrangling with just the shell
    - a shell script with as few external dependencies as possible
    - fetch and stash remote data file via curl
        - unzip/gzip if necessary
    - xsv to filter and extract and sort
    - ripgrep to transform
    - calculate a number.top 5
    - visualize via spreadsheet
    - refine/compact as a one-liner


- Your system/shell environment
    - sudo
    - installing and running binaries the old fashioned way (i.e. no homebrew)
    - understanding the system path
        - which
        - echo $PATH
        - adding to the sys path
    - very very basic shell scripting concepts
        - what are variables
        - very basic functions – basically, a way to name sequence of commands
            - maybe introduce function arguments(?)
    - .bash_profile/.zsh/etc
        - how to configure your prompt
        - set environment variables
        - add functions
        - maybe configure the environment path? 

- Packaging code as a script
    - What is a script?
        - What makes a script different than a text file?
        - (optional) what is an executable?
        - `chmod a+x` for fun
    - Repeatable scripts are good
        - stop copy-pasting shit from Stickies
        - how to generalize a list of commands to something flexible
        - make a script easier to use with command-line args
    - Make your own custom shell script
        - make it globally accessible via system path

- GIF making script
    - a shell script that's more fun, but more complex external dependencies
    - youtube-dl/curl a video
    - ffmpeg/convert into image files
    - stylize the images
    - make a gif
    - turn it into a giffy-like util


### Unit 4.5 Real-World Software Engineering

Considering the world beyond our Terminal, including web resources and remote collaboration and how to keep projects sane when you have multiple collaborators.


- Getting data from a Web API
    - what is an API?
        - actually, what is not an API
        - why sites put data into JSON
        - [todo] get sample JSON data files
        - [todo] figure out a public data API that doesn't require auth
    - http concepts
        - GET vs POST
        - HTTP status codes
        - query parameters and data payloads
        - Using the web dev tools to discover unofficial APIs
    - advanced curl
        - curling into files (i.e. why we don't need/use wget)
        - configuring web-agent
        - sending a data-payload and using POST

- Version control and git
    - https://missing.csail.mit.edu/2020/version-control/
    - Why version control? Why git?
        - why git
    - .gitignore
    - git CLI basics and concepts
        - git init
        - git add
        - git commit
        - git status
    - what's in .git?
    - rolling back in history
        - git checkout

- Clouds as a service

    - Github
        - README.md convention
            - More Markdown fun
        - Github pages
        - Gists
        - Pull requests
        - How to contribute to open source
            - correct grammar changes in someone else's project
    - AWS
        - S3
            - access-control concepts
            - how to quickly upload files from the command line
            - using S3 as a static file server
        - cloud services, like speech2text and image classification
            - fun with JSON

    - Distributed/collaborative work (i.e. why Github)
        - note: this stuff is hard to grasp until you're actually doing a collaborative project
        - Command-line Github
            - generating a new ssh key https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
            - git remote
            - git clone
            - git push
            - git pull
        - what is a git conflict
            - why do they happen
            - how to deliberately make a conflict
            - how to resolve a conflict
    - git branch/checkout ?


### Unit 5: Higher-level scripting

Actual programming – e.g. learning Python or R or Javascript or even SQL – is beyond the scope of this project. However, shell scripting basically is programming. So the aim of this unit is to help you get started on getting into a "proper" language, and to give you a taste of *why* you'd want to do it – which can be hard to convey if you've seen the amazing usefulness of shell scripting.


- R and RStudio
    - RStudio seems much easier and straightforward to install for the average user, compared to Python (even with conda)
    - RStudio basics
        - why R syntax is NOT the same as shell syntax
        - variables and variable assignment
        - quoting strings
        - functions
    - How to do cool stuff with ggplot2
        - use built in datasets like iris
        - switching between chart types
        - tweaking colors
        - making PNGs
    - Data wrangling basics
        - dataframes
        - opening files (CSV, XLS)
        - saving files as CSV

- Web scraping with R
    - enough HTML concepts to understand why regex is not enough
    - CSS selector
    - xpath for funsies
    - how HTML turns into data
        - copy-pasting HTML tables into a spreadsheet
        - scraping non-tabular HTML into CSV
    - [todo] mirror a website to practice on

- R outside of RStudio
    - just use VSCode 
    - running R scripts from the commandline
    - reproducible data->viz R script
    - rmarkdown? 

- SQLite
    - Using a GUI like DB Browser
        - Why SQL and not Excel? 
    - Basic SQL syntax
        - SELECT queries and how they compare to spreadsheets
    - SQLite without a GUI
        - invoking sqlite3 from the command line
        - dot commands/config
        - turning sqlite into a CSV
    - optional (combining sqlite scripts with R scripts to make viz)    


 
### Unit 6: The Big Picture

Tying it all together, with some kind of contemporary real-world data project

- FEC contribution data
    - Creating a project folder
        - how to organize stuff
        - how to name stuff
    - Getting the data
        - Downloading from the API
        - Bulk downloading from the bulk site
    - xsv to filter and organize
    - ggplot to chart
    - Markdown to publish on Github
    - Converting all previous steps into a reproducible data pipeline as a shell script

- Grepping videos for phrases
    - curl/youtube-dl to fetch video
    - ffmpeg to strip audio
    - cloud service for voice-recog 
    - clean and filter the resulting data JSON with regex (as much as possible b/c teaching JSON parsing is beyond the scope for now)

- Your Life as Data
    - how to download from Google/Twitter/FB/Apple
    - analyze and visualize your life





## Resources

- http status cats: https://http.cat/

- VS Code: https://code.visualstudio.com/

- How to be a Better Web Researcher via Dan Russell: https://blogs.scientificamerican.com/observations/how-to-be-a-better-web-searcher-secrets-from-google-scientists/

- RegExr interactive regex editor: https://regexr.com/

- MIT Missing Course videos on shell scripting:
    - https://www.youtube.com/watch?v=Z56Jmr9Z34Q
    - https://www.youtube.com/watch?v=kgII-YWo3Zw

- Data Carpentry https://datacarpentry.org/

- Julia Evans' zines https://wizardzines.com/
