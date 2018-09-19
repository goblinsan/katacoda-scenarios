# Katacoda Theia IDE
This is an example of using Theia as an IDE with Katacoda


## index.json
For this we are using the beta theia image
and testing the iframe-terminal layout

```
    "environment": {
        "showdashboard": true,
        "dashboards": [{"name": "IDE", "port": 3000}]
        "uilayout": "terminal-iframe",
      },
      "backend": {
        "imageid": "theiaide",
        "port": 3000,
      }
    
```