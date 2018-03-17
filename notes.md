`kaggle competitions download -c house-prices-advanced-regression-techniques`

use -p for download path. Defaul download location- ~/.kaggle


Deleting Files using Git/GitHub"
`git add . -A `
Next:
`git commit -m "removed some files"`

or

`git add -u
git commit -m "Removed some files"
`

-u, --update
           Update the index just where it already has an entry matching
           <pathspec>. This removes as well as modifies index entries to
           match the working tree, but adds no new files.

           If no <pathspec> is given when -u option is used, all tracked
           files in the entire working tree are updated (old versions of Git
           used to limit the update to the current directory and its
           subdirectories).

       -A, --all, --no-ignore-removal
           Update the index not only where the working tree has a file
           matching <pathspec> but also where the index already has an entry.
           This adds, modifies, and removes index entries to match the
           working tree.

           If no <pathspec> is given when -A option is used, all files in the
           entire working tree are updated (old versions of Git used to limit
           the update to the current directory and its subdirectories).




You can see deleted files, which are still 'tracked' with:

git ls-files --deleted
To delete files from a branch, you can do something like this:

git ls-files --deleted -z | xargs -0 git rm
From man git-rm:

Remove files from the index, or from the working tree and the index. git-rm will not remove a file from just your working directory. (There is no option to remove a file 13 only from the work tree and yet keep it in the index; use /bin/rm if you want to do that.)

Finally, to commit the "removal" do something like:

git commit -m "removed some files"
