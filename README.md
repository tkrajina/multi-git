Multi git
=========

This is a small git plugin that enables you to execute a single git command on multiple repositories:

Usage
-----

If you have repositories ~/projects/repository1, ~/projects/repository2, ~/projects/repository3, ~/projects/repository4, ... First go to:

    cd ~/projects

Check the status of all repositories:

    git multi status

...which is the same as:

    git multi

Execute "git gui" only on repositories which contain some changes:

    git multi -c gui

Switch to "master" for all repositories:

    git multi checkout master

Create a "test" branch on all repositories and checkout it immediately:

    git multi checkout -b test

...and so on. The basic usage is simple "git multi normal_git_commands_here". In addition to this, "git multi -c git_commands" will execute "git_commands" only on changed repositories and "git multi -b" will show the current branch for all repositories.

If you want your "git multi" commands to always execute all except some repositories add them to the file ".multigit_ignore" in the same directory.

With:

    git multi -a

A .tar archive named git-repositories-yyyy-mm-dd-hh-mm.tar with all repositories in this directory (i.e. their .git directories) will be created.

Installation
------------

Copy or create a symlink of the git-multi script in your /usr/lib/git-core directory.

See also
--------

See also https://github.com/tkrajina/TinyLayerAroundGit for a eclipse project with similar functionality.
