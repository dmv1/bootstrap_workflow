bootstrap_workflow
==================

Bootstrap - Workflow

Bootstrap git repository
git clone git://github.com/twbs/bootstrap.git


Bootstrap CDN
<!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="//netdna.bootstrapcdn.com/bootstrap/3.0.0/css/bootstrap.min.css">

<!-- Optional theme -->
<link rel="stylesheet" href="//netdna.bootstrapcdn.com/bootstrap/3.0.0/css/bootstrap-theme.min.css">

<!-- Latest compiled and minified JavaScript -->
<script src="//netdna.bootstrapcdn.com/bootstrap/3.0.0/js/bootstrap.min.js"></script>


Jquery
http://jquery.com/
save this file to the ~/_/components/js folder as jquery.js

Site Folder structure
~
~/_
~/_/components
--copy bootstrap fonts, js, less folder to this components folder
--delete the test folder in the bootstrap js folder
-- add jquery.js to the js folder here
~/css //this will hold the compress version of the less files
~/js //this will hold the compressed version of the js files
-- move the fonts folder this the ~/_ folder
~/images
~/index.php file

## Need to compress js files and combine less files into a css file before you can use the framework
## Use Codekit - https://incident57.com/codekit/ (can also do this with grunt on cli)
-- set up prefs 
-- remove refresh projects automatically -> set to never
-- turn off safari and only run active tab in chrome

-- grab the entire project folder and drag and drop into codekit window
-- change path for the output of the less files (under the styles tab) -> right click and set output path the _/css and change style to compressed (minified and compressed)
-- output filename is bootstrap.css (this actually pulls in the other less files)
-- hit compile to compress all less files

-- create a separate css file for your styles
-- create this file in the less folder, call it _mystyles.less
-- return to codekit, refresh and you see the new file
-- select it, uncheck the do not compile directly (right side), change output path to css folder and remove the underscore, choose compressed

-- delete the import lines in the bootstrap.less file if you are not going to use the components in your site to reduce the file size

## Similar workflow for javascript code in codekit
-- make sure you look for plugin dependancies with the javascript
-- check the Do not compile directory button to make a single file

--  create a new file in components/js called _bootstrap.js
-- at the top of this file, create the following 

// @codekit-prepend "jquery.js" (this is the exact way to add these)
add other dependancies in the same way
make sure the order is correct

also create a separate document to hold your own javascript 
add new file _myscript.js in components/js folder

refresh in codekit

uncheck do not compile directly
right click on the two aforemented files and choose path to _/js, remove _ from filename
also uncheck the check with jshint, concat -> minify

the process and check for the files










