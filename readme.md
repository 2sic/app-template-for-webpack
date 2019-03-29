# 2sic 2sxc App template

This is the App template to create 2sxc apps using Webpack.

To use this template, you have to adjust a few things:
- Open webpack.config.js, in here chose which bootstrap version you use and set the variable to that.
- In the same file, give a name to your app. 
- Open your template file (.cshtml), scroll to the bottom, and change 'appname' in appname.App(...) to the name you specified before

If you've done all of this, you are ready to go. Just type 'webpack' in your console and webpack will automatically watch all your ts and scss files in the src folder.
