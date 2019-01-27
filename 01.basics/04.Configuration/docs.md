---
title: Configuration
metadata:
    description: CSYCMS focuses on making things as easy as possible for the user, and the same goes for configuration.
    author: Brian Onang'o
---


## Configuration 

CSYCMS focuses on making things as easy as possible for the user, and the same goes for configuration. There are two types of configuration files: `.env` and `system.config.js`. There is only a single `.env` for the whole system and a single `system.config.js` for each site. You can find `system.config.js` in `config/SITENAME/`. CSYCMS comes with sensible examples for all the configurations you need. These are copied during the installation to act as your system defaults.

 `system/config/system.yaml` file.

Here are the variables found in the default `.env` file:

### `.env`

`
    SITES="csycms|3000|https://github.com/csymapp/csycms-learn.git" # list of sites
`

`SITES` is a comma separated list of sites.

An entry for a single site has in order:
- site name
- port on which to server it
- the repo in which the site files are found

These parameters are separated by a `|`. To add another site, create for it its own configuration line. And add the line to `SITES=`, separating it from the last line by a comma.

`CSYCMSDOCSREPO=https://github.com/csymapp/csycms-learn.git # repo where csycms documentation is.`

You may not have to do anything to this.

`THEMESREPO=git@github.com:csymapp/csycms-themes.git # repo where csycms themes are`

Please leave also this as it is, unless you know what you are doing.

`UPDATEINTERVAL=5 # update interval in minutes`

The period for which you'd like the system to check for update for itself and for all the sites.

You can change these values while setting up the system for the first time or at any other time. Just remember to `systemctl restart csycms.service` every time you make any changes to `.env` except for the changes made during the installation.

### `system.config.js`

You will also need to make changes to all `system.config.js` in `config/*/`. Please be sure especially to change: 
 - `domain` (it is just a wrong naming which we will change later). By domain we mean the base url without the protocol. eg `www.cseco.co.ke`, `localhost:3001`, etc
 - `site`. This should be the same as the site name given in `.env`
 - `site_space`. This is used to defined sites whose content can be searched together.
 - `site_title`. 
 - `search_scope`. The value for this is either `local` or `global`. It defines where only the content for the current site is searched during a search performed on the site or the content for all the sites in the `search_space`.

 Each of these variables comes with an explanation as to what it does. Remember you will need to restart the app after changing config variables.

 ## Further Configuration

You will have to do further configuration in your pages to define:
- the theme to use for the page
- the layout to use for the page
- the page to render for the request to the page

You can see more of this on [pages](/Content)