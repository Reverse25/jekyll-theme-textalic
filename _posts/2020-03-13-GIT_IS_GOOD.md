# Git is Good
**Category:** forensic

> The flag used to be there. But then I redacted it. Good Luck. https://mega.nz/#!C483DAYB!Jjr55hfJQJ5-jspnyrnVtqBkMHGJrd6Nn_QqM7iXEuc
---
Git is Good
Category: forensic

The flag is used to be there. But then I redacted it. Good luck. https://mega.nz/#!C483DAYB!Jjr55hfJQJ5-jspnyrnVtqBkMHGJrd6Nn_QqM7iXEuc

The title clearly shows what we are going to do in this challenge, which is to use git . If not installed, please download and install git here

Extract the file that we just downloaded. After that all the file information will be extracted
```
unzip gitIsGood.zip
cd gitIsGood
ls -la
```
When entering the folder gitIsGoodthere are 1 file flag.txtand 1 folder .gitwhich indicates that this folder is a git repository . We try to read the contents of the file flag.txt.

```
cat flag.txt
```
When flag.txtread, there is a flag. But this is not the flag that we are looking for, because the flag has been edited ( redacted ).

With git we can see the editing history in the repository with the command log.
```
git log
```
From here we can see the history of editing that was done and the date and description. From here also we know that the file flag.txthas been edited 3 times.

To see the details of the changes we can use the option -p ( patch ).
```
git log -p
```
Gotcha! We can see the flag before changes are made.
```
flag: flag{protect_your_git}
