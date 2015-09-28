A Gentle Git Primer
========

When setting up a git repository, you have a few options. Either you can

    git clone some/existing/repository

or you can

    git init

in an existing directory, which will allow you to do more things with
git. For instance, to clone this repository, you would `git clone
https://github.com/EC327-Fall-2015/git-primer`.

Once you've done that, you now have a local git repository. You have a few
basic commands you'll need for making commits.

    git add path/to/file
    git rm path/to/file
    git commit

git does not track any files unless told to, via `git add`; you'll also
generally want to specify the changed files you wish to add to a commit by
adding them as well. Likewise, if you no longer wish for it to track a
file, you need to remove it via `git rm`.

Comment about `git rm`: if a file has been changed since the last commit,
you will need to specify more. If you wish to retain the file in your local
directory, specify `--cached`. If you wish to delete the file, specify `-f`
(or `--force`, if you like writing things out).

git commit takes the changes you've added and essentially creates a
checkpoint. A lazier approach is to commit all changes to tracked files by
specifying -a, but specificity is often useful. Further, if you just type
`git commit`, the terminal will open up your $EDITOR of choice and tell you
to type in a message. If you're deathly afraid of both vi and environment
variables, you can specify `-m <MESSAGE>` to enter your commit message on
the command line.

In a commit message, you can say whatever you want, although writing
meaningful commit messages will go a long way toward helping collaborators
understand what you've done and why.

Thus far, I've done the following:

    git clone https://github.com/EC327-Fall-2015/git-primer
    cd git-primer
    git add README
    git commit

Next on the roster are push and pull. For now, we'll just consider that
`git push <remote> <branch>` pushes your local commits to a remote
repository, and `git pull <remote> <branch>` pulls new commits from a
remote repository. If you cloned this repository, the nickname for the
default remote is `origin`, and the name for the default branch is
`master`. Therefore to push this commit to github, we just need to specify

    git push origin master

More on branches later.
