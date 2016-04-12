# An Introduction to GitHub
Produced by your ./CS officers!

## What is Git? What is GitHub?
Git and GitHub are two separate things.  
*Git* is a software system that is used to keep track of changes that you make to a project over time.  
*GitHub* is a web-based service that hosts Git repositories online for people to share, browse, and collaborate.
> #### Wait hold on—what's a repository?
> Oh, sorry.  
> A repository, if you look in a dictionary, is "a place where things may be stored".  
> Repositories in version control systems like Git follow the same idea; a *Git repository*
> stores information not just about your project's current files, but also its commit history.  
> #### But...what does "commit history" mean?
> Alright, we should really just get started with the tutorial, and we'll answer most of your questions along the way.

## The First Steps
First, you need to sign up for GitHub. Click the green "Sign Up" button near the top-right of the page
(although you should probably open it in a new tab) and follow their directions! Yes, GitHub has their own tutorial,
but we don't really like it.  
Next, you need to install Git on your computer. So what operating system do you have?
### Windows!
Head over to [the Git website](https://git-scm.com/downloads) to download the installer.  
Run the installer when it finishes downloading. We recommend:
- select the "Use Git from Git Bash only" option (on the fifth screen)
- unselect the "Enable Git Credential Manager" option (on the ninth/last screen
- use the defaults for everything else

### Mac!
We recommend that you install [Homebrew](http://brew.sh/) and then use that to install Git.  
Homebrew is a free and open-source package manager for Mac OS X that's incredibly useful for
installing and updating ahuge variety of computer science-related software.
### Linux!
As you probably know, it'll depend on your distribution; you can refer to [the Git website](https://git-scm.com/download/linux)
for the specific command.

## Your First GitHub Repository
We're excited and we hope you are, too!

1. Click the "+" in the upper right corner of this page, next to your profile picture, and click "New repository".
  - Again, you should probably open it in a new tab.
2. Enter a name for the repository, maybe something like "Hello-World"
  - Definitely use "Hello-World". It will make this tutorial less confusing.
3. Enter a description if you'd like
4. Make it a public repository
  - Public is free and free is good.
5. Do not select "Initialize this repository with a README".
6. Don't add a .gitignore, don't add a license.
7. Go ahead and click "Create repository".

## Your First Git Repository
The excitement just keeps building!
> #### Wait, didn't we just do this?
>No. Remember, Git and GitHub are separate things.

1. Open up command line
  - If you're on Windows, open up the Git folder, which is in your Program Files folder, and execute **git-bash.exe**.
  - If you're on Mac, open up **Terminal**.
    - You can find it in the Utilities folder, which is in your Applications folder.
  - If you're on Linux, you know what to do.
2. Navigate to your Documents directory by using the command `cd ~/Documents`.
3. Create a directory named "GitHub" by using the command `mkdir GitHub`.
4. Navigate into this new directory by using the command `cd GitHub`.
5. Create a directory for your repository, again using the `mkdir` command.
  - Maybe name it "Hello-World".
  - Yeah, definitely name it "Hello-World".
6. `cd` into your new directory.
  - If all of this is new to you, we recommend taking a look at
  [Command Line course on Codecademy](https://www.codecademy.com/learn/learn-the-command-line).
  - Codecademy also has a [course on Git](https://www.codecademy.com/learn/learn-git), but we also don't really like that one.
7. Use the command `git init`.
  - This initializes a Git repository in your directory. In other words, it sets it up to use Git.
8. Use the command `git config --global user.name "[Firstname] [Lastname]"`.
  - Replace `[Firstname]` with your first name, and `[Lastname]` with your last name
  - This helps Git identify you.
9. Use the command `git config --global useremail "[youremail@whatever.yes]"`.
  - Replace `[youremail@whatever.yes]` with your email address.
  - This command connects this Git repository with your GitHub account.
10. Use the command `git status`.
  - Nothing too exciting at the moment. Notice it says "nothing to commit". That's because our directory is empty!
11. Use the command `echo "# Hello, World" >> README.md`
  - The `echo` command outputs a string onto the command line. Our string here is "# Hello, World".
  - The `>>` command redirects output to a text file. Our file here is README.md.
  - So now we have a file README.md which contains the text "# Hello, World".
12. Use the command `git status` again.
  - Oh my God, there's red text!
  - It's alright; Git is saying that there's a new file in the directory, and we haven't told Git what to do with it yet.
13. Use the command `git add README.md`.
  - We're now adding README.md to the repository.
  - If you're on Windows and you get a warning about replacing LF with CRLF, don't worry. The reason behind it is
  [complicated](http://stackoverflow.com/questions/1967370/git-replacing-lf-with-crlf/20653073), but it won't cause any real
  problems for us.
14. Use the command `git status`.
  - Now it's green! It lists README.md under "Changes to be commited." We made the change. Now we have to commit it.
  
  > #### This tutorial is sooo long.
  > What?
  > #### This tutorial is way too long.
  > Alright yes, it's kind of long, but there really is no faster or shorter way to teach Git effectively.
  > All those "Learn Git in 10 minutes" tutorials tend to skip some pretty important details.
  > Plus, we spent quite a bit of time signing up for GitHub and installing Git.
  > A lot of other tutorials don't really care about that part, but we do.  
  > Your Dot-Slash officers care.  
  > And trust us, this is worth it. We promise.

15. Use the command `git commit -m "First Commit!"`.
  - `git commit` finalizes the changes we make to Git. Think of it like *committing* to a decision.
  - The `-m` part is called an *option* to the `commit` command. This lets us add a commit message; here, it's "First Commit!".
  - Commit messages are [*very* important](https://xkcd.com/1296/); they let you keep track of changes you make to a project.
16. Use the command `git status`.
  - Git might say something like "nothing to commit, working directory clean". That just means we've already committed everything there
  is to commit.
17. Use the command `git remote add origin [repository_url.git]`.
  - Replace `[repository_url.git]` with the url of the GitHub repository we made earlier.
  - You can find it on your repository's webpage, or you can use the url of that webpage and add .git to the end.
  - It should look something like this: `https://github.com/username/Hello-World.git`.
18. Use the command `git push -u origin master`.
  - Now we're *pushing* our changes from our local Git repository to our online GitHub repository.
  - The `-u` option is short for "upstream", which refers to the repository you're linking to; in the future, when you work in this
  Git repository, you only need to type `git push` instead of that full command, and Git will know where to push your commits.
  - Git will ask for your GitHub username and password; Git by itself doesn't have permission to modify your GitHub repository, so go
  ahead and enter your login credentials.
19. Use the command `git log`.
  - This displays a history of your commits in your local Git repository.
20. Go to your GitHub repository in your internet browser.
  - You'll be able to see your latest commit, as well as "Hello, World" in large lettering in the bottom half of the page.
21. Feel a sense of accomplishment.
  - You're amazing. You really are!
  
## The Conclusion
Now you can start using GitHub to publish your projects and provide updates on your progress!  
Just remember that making changes to your GitHub repository has three steps: `add`, `commit`, and `push`.  
There's still more to learn, specifically cloning, pulling, forking, and merging, but those are slightly more advanced topic that will
be added later. For now, happy hacking and go be creative!

## By the Way...
One important thing to note is that *your work on GitHub is public*. Your code is available to anyone who's interested, unless you'd
prefer to pay for an account upgrade to use private repositories. But this doesn't mean that other people can freely steal your code.
Remember when you made your GitHub repository and we told you to not add a license? Well, you can add add
[an open-source license](http://choosealicense.com/) to protect your work. And even if you don't add a license, your work is still
protected by standard copyright laws. Your GitHub repository and your commit history is proof that you own your code.
