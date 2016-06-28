Installation
==========================================

## Prerequisites

Make sure Composer is available, or [download it](https://getcomposer.org/download/).

`webroot/mfz-rules` is the folder where we will set up the site. Your webserver should have access to it. A "real-life" path could be something like `/var/www/mfz-rules` for instance.


## Grav : download the framework using composer

You can create a new project with the latest **stable** Grav release with the following command:

```
$ composer create-project getgrav/grav ~/webroot/mfz-rules
```

This will create the `mzf-rules` folder and download Grav.

> See [the official repo](https://github.com/getgrav/grav) for more ways to get Grav.
 
## mfz-ra-rules : git goodness

Let's now get the mfz-ra-rules project into our fresh Grav install :
```
$ cd webroot/mfz-rules/user
$ rm -rf ./*
$ git init
$ git remote add origin https://github.com/jdubuisson/mfz-ra-rules.git
$ git pull origin master
```

> We delete the content of `user\` before the git setup to avoid any collision.
 
## Learn2 : get the theme through GPM

In the root of the Grav install (`webroot/mfz-rules`) type :

```
$ bin/gpm install learn2
```

This will install the Learn2 theme.

## Plugins

Various plugins are used to provide addition functions.
In the root of the Grav install (`webroot/mfz-rules`) type :
```
$ bin/gpm install markdown-notices
$ bin/gpm install breadcrumbs
$ bin/gpm install simplesearch
$ bin/gpm install langswitcher
```

> markdown-notices : Provides notices in MD format using !, !!, !!!, !!!!
>
> breadcrumbs : Provides Breadcrumbs.
>
> simplesearch : Provides search functions, effectively removing pages from the sidebar if they don't match the search string.
>
> langswitcher : provides native language text links to switch between Multiple Languages in Grav 0.9.30 or greater.

## That's it

You're all set up now. Open up a browser and access the URL that points to `webroot/mfz-rules` and you should see your install of the rules.

If it is not the case, you should check that `webroot/mfz-rules` is accessible by your webserver user/group.