---
layout: post
title:  "Automatic site creation"
date:   2014-11-30 16:48:45
comments: true
categories:
description: During development I quite often purge Alfresco database and after each purge I need to manually recreate all the content that has been deleted such as sites, peoples, folders and so on. In this post I'd like to show how to create sites automatically with a simple webscript.
tags:
- alfresco
---

Usually when you develop some new features for Alfresco quite often you need to completely clean the project and purge database. Which is not so good since you will loose all manually created things such us folders, users or sites. With sites it could be quite complicate to manually recreate them. In this post I'll to show how to create sites automatically using webscript. So instead of creating sites one by one, manually insert names and privacy settings you'll just need to call a webscript. And also with this method you could be sure that all your sites are in place.

I found few tutorials on how to do this, but some of them were too complicated, some just didn't work. First thing which probably could do the work is `siteService` in repo project. But the problem with it that it only creates site on repo side. So share wouldn't know anything about it. Another approach which worked for me is to use `create-site` webscript. It is a POST webscript, so you'll need to pass all the site parameters to it.
