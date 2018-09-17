This is your first step.

## Task

This is an _example_ of creating a scenario and running a **command**

`echo 'Hello World'`{{execute}}

    
`docker run -it -u root --name theia \
    -p 3000:3000 -v "$(pwd):/home/project:cached" theiaide/theia-java`{{execute}}


Render port 8500: https://[[HOST_SUBDOMAIN]]-3000-[[KATACODA_HOST]].environments.katacoda.com/