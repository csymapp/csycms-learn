---
title: Installation
metadata:
    description: We have created an installation script which you can use to install CSYCMS
    author: Brian Onang'o
---


## Installation 

Once you are sure you have met the [minimum requirements](/basics/Requirements) you can install CSYCMS by following these steps:

We have created an [installation script](https://raw.githubusercontent.com/csymapp/csycms/master/Install/installCsycms.sh) which you can use to install CSYCMS. 

```bash
cd /tmp
wget https://raw.githubusercontent.com/csymapp/csycms/master/Install/installCsycms.sh
chmod +x installCsycms.sh
./installCsycms.sh
```

Then follow the installation instructions as directed by the script. This will create the csycms files in `/var/www/html/csycms` and create `csycms.service`.

You will have to edit [some configurations](/basics/Configuration) before you can start creating your sites.