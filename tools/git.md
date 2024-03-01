# Commits

If you're in the middle of editing a commit (such as by calling `git reset
HEAD^`, but you want to retain the commit message of that commit that you're
editing given it will be lost at the point where you call `git commit`, you can
do the following:

1. Make the relevant changes that you require
2. Enter the reflog (`git reflog`) and find the title of the commit that you're
   editing - as recent as possible
3. Stage your changes
4. Call `git commit -c HEAD@{n}` where `n` is the position in the reflog of the
   commit that you're editing.

You'll then see that the commit message gets automatically populated, and you
don't have to copy-paste/type it out manually from elsewhere.
