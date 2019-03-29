# 2sic 2sxc App template

This is the App template to create 2sxc apps using Webpack.

## Basic Concepts and Ideas

1. All our js/ts code is typescript in the `/src` folder
1. All our css is generated using SASS, the originals are also in the `/src` folder
1. Everything us built using Webpack to fully automate our work
1. The basic idea is that we can build for Bootstrap3 and 4, so we have both a bs3.scss and bs4.scss. If you're creating a **standard-app** for distribution, you'll want to maintain both. If you only want to create an app for a specific site, you'll only want to use one

## Polymorph Editions and Building into Different Targets

1. We use Polymorph Editions to publish it, so there is a...
   1. ...`/live/dist` is for production. the main references should point to this
   2. ...`/staging/dist` is for code which we're working on (incl. open-heart surgery) - so if you're working on a production site, build to this, and ensure that host-users or similar load this, while the end-users still get the original file
1. To build into these folders, the following `npm` commands are prepared
   1. `npm run watch-live` will watch & build to `/live/dist`
   2. `npm run watch-staging` will watch build to `/staging/dist`

## Before you Get Started

Your setup must have nodeJs, npm, webpack and typescript, ts-loader and sass-loader installed - if you are missing something, follow https://azing.org/2sic/r/632kqgG3 

## Getting Started

To use this template, you have to adjust a few things:

* Change the name of your javascript module for this app

  1. Open webpack.config.js, in here chose which bootstrap version you use and set the variable to that.
  
  1. In the same file, give a name to your app.

  1. Open your template file (.cshtml), scroll to the bottom, and change 'appname' in appname.App(...) to the name you specified before

* Update the reference to the `_variables.scss` which should take parameters from your theme. You can find this in TODO 2lt

If you've done all of this, you are ready to go. Just type 'npm run watch-live' in your console and webpack will automatically watch all your ts and scss files in the src folder.
