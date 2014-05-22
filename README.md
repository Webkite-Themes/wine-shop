Webkite Theme Globals
=====================

This project contains the global files for creating themes.  To create
your own theme or themes:

1.  Create a new git repository however you care to do so.

2.  Add this repository as an alternate remote:

        git remote add theme-globals git@github.com:Webkite-Themes/contact-list.git

3.  Fetch and merge the global files.

        git fetch theme-globals
        git merge theme-globals/master

4.  Add your own theme code in an appropriate subdirectory.  See
    contact-list as an example.  It contains three theme directories
    complete with manifest files.

5.  Build away!

Updating your global files
--------------------------

Your global files will never be implicitly updated.  If you want to
update these so that new features and bug fixes are available:

1.  Update the theme-globals remote:

        git fetch theme-globals
        git merge theme-globals/master

    or update to an explicit tagged version:

        git fetch theme-globals
        git merge globals_1.0.0

Adding globals to an existing repository
----------------------------------------

If you are migrating an existing legacy theme:


1.  Add this repository as an alternate remote:

        git remote add theme-globals git@github.com:Webkite-Themes/contact-list.git

2.  Fetch and merge the global files.

        git fetch theme-globals
        git merge theme-globals/master

4.  Create a new subdirectory for your theme:

        mkdir table

5.  Move appropriate files to this subdirectory and delete the others.

6.  Commit the changes and push:

        git add .
        git commit -m"Initial conversion to theme-globals"
        git push origin master

