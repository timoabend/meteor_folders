#Folder-Skeleton for Meteor.js
##With explanation and processing-order of files 
Source: [Meteor Documentation](http://docs.meteor.com/#structuringyourapp), 
Version 
* 8.2
* 8.3

####Folders
```
.
|-private				files being loaded into Node.js, available via Assets-API
|-public				images, favicon.ico, robots.txt, ..
|-server				only available in server-scope
|-client				only available in client-scope
|  |-compatibility		loaded into global scope of client
|-test					files from folder test are not being loaded
```

####Files being loaded in order
1. private/*.js loaded into Node.js
2. *.js except client/ public/ private/
3. private/*.* loaded and available via Assets-API
4. client/compatibility/*.js being loaded into global scope of client
5. *.css
6. *.html -> scan for head, body, template

####General order files are being processed in a directory
1. lib/
2. subdirectories
2. files in alphabetical order
3. main.*
