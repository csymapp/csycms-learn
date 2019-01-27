---
title: Testing
metadata:
    description: CSYCMS is a Fast, Simple, and Flexible, file-based content management system, knowledge base and static site generator for nodejs.
    keywords: csycms, file-based content management system, knowledge base, static site generator, nodejs
    author: Brian Onang'o
---


## Testing

Assuming you successfully [installed CSYCMS](/basics/Installation), a service will be created which will run the whole thing for you. 

But in case you want to test independent of the service then you may run:

```bash
PORT=3001 SITE=csycms DOMAIN=localhost:3001 node bin/app.js
```

Then view localhost:3001 in your browser. You may replace 3001 with any other port and csycms with any other valid site that you have installed.