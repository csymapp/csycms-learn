---
title: Processes
metadata:
    description: CSYCMS is a Fast, Simple, and Flexible, file-based content management system, knowledge base and static site generator for nodejs.
    keywords: csycms, file-based content management system, knowledge base, static site generator, nodejs
    author: Brian Onang'o
---


## Processes

`csycms.service` starts several process:

- `csystemUpdates` which checks for updates to the entire system and to themes.
- `monitors` which act as monitors for every site, restarting server instances for every site on failure. Each site has a monitor.

Each monitor starts:
- The node server: `PORT=$PORT SITE=$SITE DOMAIN=$DOMAIN node bin/app.js --SITE=$SITE &`. Each site has this process.
- `siteUpdates` which checks for updates for each specific site and restarts the node server for the specific site if updates have been done. Each site has a `siteUpdates` process.