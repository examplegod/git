# git

[git clone, git init](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)

[git status, .gitignore, git rm, git mv](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)

[git log := source tree workspace/History](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History)

[source tree History, Search](https://gitbook.tw/chapters/using-git/log.html)

[git commit --amend, git reset HEAD, git checkout](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)

[git remove GitHub fetch push remove rename](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)

[source tree remote](https://gitbook.tw/chapters/github/push-to-github.html)

[git tag](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

[github tag](https://zlargon.gitbooks.io/git-tutorial/content/advanced/tag.html)

[Git Basics - Git Aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)


## Git Large File Storage (LFS) 
Homebrew: brew install git-lfs

### Getting Started

Download and install the Git command line extension. Once downloaded and installed, set up Git LFS for your user account by running:

> $ curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash  
$ sudo apt-get install git-lfs  
$ git lfs install

>$ git lfs install

You only need to run this once per user account.

In each Git repository where you want to use Git LFS, select the file types you'd like Git LFS to manage (or directly edit your .gitattributes). You can configure additional file extensions at anytime.

>$ git lfs track "*.psd"

Now make sure .gitattributes is tracked:

git add .gitattributes
Note that defining the file types Git LFS should track will not, by itself, convert any pre-existing files to Git LFS, such as files on other branches or in your prior commit history. To do that, use the git lfs migrate[1] command, which has a range of options designed to suit various potential use cases.

>$ git lfs migrate import --include="*.obj"

else no migrate error
```config
remote: Resolving deltas: 100% (8/8), completed with 4 local objects. remote: error: GH001: Large files detected. You may want to try Git Large File Storage - https://git-lfs.github.com.
remote: error: See http://git.io/iEPt8g for more information.
remote: error: File <files> is 119.80 MB; this exceeds GitHub's file size limit of 100.00 MB
```

There is no step three. Just commit and push to GitHub as you normally would.

> $ git add file.psd  
$ git commit -m "Add design file"

check status

>$ git lfs ls-files
