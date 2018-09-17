This is your first step.

## Task

This is an _example_ of creating a scenario and running a **command**

`echo 'Hello World'`{{execute}}

    
`docker run -d -u root --name theia \
    -p 3000:3000 -v "$(pwd):/home/project:cached" theiaide/theia-java`{{execute}}
