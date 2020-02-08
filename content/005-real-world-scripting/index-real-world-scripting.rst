********************
Real world scripting
********************


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
