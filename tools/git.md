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

# Config file

Git defaults to searching up from the current working directory for the
`.gitconfig` file - this means that you can build a tree of configuration files
to ensure each directory uses the exact settings that you require.

A nice way around this is to forego having a `.gitconfig` file in your home
directory, and then have one for your `work` and `personal` directories. The
only catch here is when you want to clone something into your home directory;
you have two options:

* clone the repository in either the `work` or `personal` directories
  (depending on the account that you want to use) and then either move it or
  symlink it to your destination of choice

* manually input the configuration information at the point when you want to
  clone the repo, which can take much longer (and you'll have to do this every
  time you want to clone outside of a directory that contains a `.gitconfig`
  file).


