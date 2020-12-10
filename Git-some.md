# "GIT" while the gittin' is good...

## What's a Version Control System (VCS)?

A VCS is a system that allows you to revisit changes to files or sets of files. This is important because it prevents the loss of data while tracking updates or changes to a file or files. 

There are various types of VCS:

    - Local Version Control System (LVCS)
    - Central Version Control System (CVCS)
    - Distributed Version Control System (DVCS)

GIT is a Distributed Version Control (DVCS) system that creates snapshots of changes to files stored in repositories on the GitHub platform. 
Linus Torvalds, the chief architect of the linux kernel, created GIT in 2005 in response to the company that managed Bitkeeper cancelling the free use of its service.
Here's a chart of the workflow GIT uses. 

![GIT Workflow](https://blog.udemy.com/wp-content/uploads/2015/08/image066.png)

Using GIT we can make changes to files by cloning our files stored on the repository located online at GitHub using the ```git clone https://abc.net/example/dontclickme``` command. 

The address to each repository is unique. This is the checkout process that clones from the Repository to our local hard disk by using the ```git clone Https:...``` at the command window prompt.  

Now we can begin to make changes to files found in the repository stored on our local machine through a text editor. I'm using Microsoft's VS Code editor on my machine but you use whatever you feel comfortable with. 

See [Choosing A Text Editor](/Choosing-text-editor.md)

At the command window prompt type ```git add nameoffile.md```  
This will tell GIT to add the changes you've made and place the file in a modified catergory. Using ```git status``` will show the file that has been modified as red. 

You're now ready to commit the changes to be stored in the staging area of our workflow chart. Go back to the command prompt and type:
``` git commit -m "Leave a message that explains why you made changes"```

This will commit the changes and alert anyone else who might be working on the file what you did and why.

Next it's time to finally push the changed file back to the online repository. Go to the command prompt and type:
```git push origin main```

You will be prompted for your GitHub username and password. Once entered, the changes will then be updated at the online repository. You can verify the changes by checking the website!

GIT is a great tool to use and is also widely used by most coders in the open source community. 

[Previous Page](/Choosing-text-editor.md)

[Back To Table of Contents](/README.md)
