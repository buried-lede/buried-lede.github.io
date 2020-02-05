# The Buried Lede of Data Journalism and Learning to Code

Inspired by MIT's ["Missing Semester of Your CS Education"](https://missing.csail.mit.edu/) (related HN thread / tweet thread), but tailored to folks who aren't learning computer science as a career or degree program – in other words, people who want to learn programming to be better at whatever their current job or passion.




## Syllabus (brainstorm in progress)

Random brainsplurge, covering whatever big ideas (what is data) and pedantic minutiae (how many bytes does a PDF scan have) I could brainstorm in 15 minutes.

For now, MacOS-focused, then generalized/translated for Win10.



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

- The Command Line, an intro for immediate everyday usage
    - Tab to autocomplete
    - super useful command-line utilities
        - youtube-dl 
            - output different title
            - get audio only
            - get subtitles
        - curl
        - wget
        - ffmpeg / convert
        - whois
        - ping

    - MacOS specific utilities
        - open
        - pbcopy and pbpaste
        - screenshot
        - say
        - brew

- The Command-Line life
    - Using Terminal
    - Keyboard shortcuts
        - command history
        - Tab to autocomplete
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
        - man
        - hist
    - VS Code + Shell
        - using `code` to open from the command line

- The Unix Way
    - Be good at one thing and one thing only
        - why unix utils seem so basic
        - as a general design and programming philosophy
    - common nix utils
        - cat
        - grep
    - pipe operator
        - pipe pipe pipe
        - cat | grep all the things
    - file redirection
        - the dangers of unix

- Shell nerdery
    - very very basic shell scripting concepts
        - what are variables
        - very basic functions
    - understanding your system path
        - which
    - sudo
    - .bash_profile/.zsh/etc
        - how to configure your prompt
        - environment variables

- Real-world data work 
    - (get a taste of doing "real" work before diving too deep into details of software dev)
    - CSV wrangling
        - xsv (or csvkit)
        - tsv to csv
        - grepping by column with regex
        - xsv to Google Sheets (no mouse, keyboard only!)
    - SQLite
        - Using a GUI (DB Browser)
        - Shell operation

    - RStudio and R (because installing R environment is likely easier than python)
        - quickie ggplot2 fun
        - running R scripts from the commandline
        - rmarkdown? 

- Advanced text editors
    - Project sidebar
    - Customization
    - Grepping and file search
    - Syntax-specific snippets/tab completion
        - Emmet for HTML (already built-in for VS Code)
    - Plugin ecosystem

- Git
    - https://missing.csail.mit.edu/2020/version-control/
    - Why version control?
    - Intro to Github
        - Markdown
        - Gists
    - Command-line Git and Github
        - generating a new ssh key https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
    - Why distributed version control?
    - .gitignore
    - git branch/checkout

- Tying it all together, i.e. the big picture
    - Some kind of real-world data project that shows how all the taught skills tie together
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

    - Web scraping via regex
        - (todo) figure out a public site with well-formed (i.e. regexable data) data
        - wget and mirror a site locally (i.e. what is caching and why you need to care)
        - VSCode
            - Managing your code, and the mirrored site, as a VS Code project
            - trying and tweaking regex patterns to figure out data patterns
        - Command-line data wrangling
            - use ripgrep to extract data and print out in a delimited pattern
            - use xsv to convert to formal CSV
        - Do some visualization/analysis via spreadsheet or R
        - Create a reproducible data pipeline with shell scripting, going from ripgrep->xsv->RScript->visualization



## Resources

- VS Code: https://code.visualstudio.com/

- How to be a Better Web Researcher via Dan Russell: https://blogs.scientificamerican.com/observations/how-to-be-a-better-web-searcher-secrets-from-google-scientists/

- RegExr interactive regex editor: https://regexr.com/

- MIT Missing Course videos on shell scripting:
    - https://www.youtube.com/watch?v=Z56Jmr9Z34Q
    - https://www.youtube.com/watch?v=kgII-YWo3Zw

- Data Carpentry https://datacarpentry.org/

- Julia Evans' zines https://wizardzines.com/
