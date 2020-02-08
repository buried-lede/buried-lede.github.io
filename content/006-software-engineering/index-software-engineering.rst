
********************
Software Engineering
********************


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
