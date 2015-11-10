# Proper Version Control
Hi! This is just a (hopefully) short README	on proper version control since version control is prone to abuse ***sad face***. Feel free to update!
### 1. Let's talk about `git add .`
Don't do it. It's better to add files one at the time. For example, you want to add all of these files:
```
hello.css
world.js
```	
It's tempting to do `git add .`, but a better solution would be to do...
```
git add hello.css
git status
git add world.js
git status
```
This allows you to keep track of the files you add rather than just dumping it. It's good practice. If you have a super long file to add, you can type the first 3-4 letters then `<tab>` to complete it automatically. 

### 2. `git diff`
`git diff` allows you to view your changes. It is recommended that you use it with `git add` and `git status`. It helps you keep track of the files you should (and shouldn't) add. 

### 3. Branches and pull requests
Do not commit straight to `master`. We want to keep master clean so it's better to commit and push to branches. Once you have pushed something to a branch, you can go to the repository and make a pull-request. Please DO NOT merge until someone approves of it. To learn more about branches, check [this](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) out.

Once a branch has been merged to master, please update your local repo using `git pull origin master`.

### 4. Limit your commits
We don't want 1 billion commits floating around because it makes things messy. If you're the type of person who like to work with multiple commits, please rebase and squash your commit one tidy commit. To learn more about rebasing, check [this](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html) out.

### 5. Good commit and pull-request messages
If you completely changed a huge chunk of CSS in one of the files, it's probably not a good idea to just type `changed css` as your commit or pull-request message. A good commit/pull-request message is one that concisely, but properly communicates the changes you made. So back to the huge chunk of CSS you changed, a better commit message would be `added position fixed to the header, changed the background color of the schedule, and added a smooth hover transition to the links`  

### 6. Merge conflicts
FML. Merge conflicts are usually caused when two people alter the same piece of code. We want to avoid this as much as possible. The solution: Let someone know when you're fixing the code. If you do run into merge conflicts, use your code smarts and decide which code should be used and which should not. A merge conflict normally looks like this:
```
.header 
	background-color: azure
	padding: 30px

	p.hello
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<< HEAD
		color: black
=====================================
		color: blue
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>> commit# or branch name
```
The code below `HEAD` and above `commit# or branch name` is the one causing problems. Figure out which code should be used and delete the lines with `HEAD`, `=====`, and `commit# or branch name`.

I thought this was important to put here since merge conflicts seem very confusing at first glance.

==========================================

If you learn any more good version control practices, feel free to edit this README! If you have any questions about Github or version control, ask [Chuk](http://www.brianch.uk/), [Dana](http://danagilliann.me/), or [Chelsea](http://chelseavalentinesday.com/).