# CLICK BC RPi
Welcome to CLICK BC RPi repo for PAT. 

# How do I clone?
Make sure to add your id_rsa.pub (public rsa key) to your git account otherwise this will not work!!!! 
Click the 'Code' drop down in the repo page and copy the text given when you select ssh. AKA:
```
git clone git@github.com:MohamedSquare/CLICK-BC-RPi.git
```
In your terminal paste this line and it will download the repo. 
Cool - Now you want to make your first commit to the repo. Navigate to the folder for this repo that you downloaded then edit the README.md

```
echo "WRITE THE SUBSYSTEM YOU WORK ON HERE" >> README.md
```
This will insert a newline into the README.md document. 
```
git add README.md
```
This will add the changes me and stage them to push to our repo. Before we commit its good practice to leave a comment about what you just did. But first lets check what files you've changed, sometimes we've accidentally edited files that we didnt mean to and wouldn't want to push that:
```
git status 
```
You should see <span style="color:red">"modified: README.md"</span>.

OK lets commit our changes and leave a message then push
```
git commit -m "YOUR-NAME my first commit!"
git push -u origin main
```
*origin* is the conventional shorthand name of the url for the remote repository (usually in GitHub or another cloud git repository provider) for your project. *main* refers to the branch of the project --(ideally each person will make a branch to work on a copy of the main codebase and then continously integrates their branch into main branch with others. For now Ill show you how to push main.)

Now you should have successfully pushed! Go check the repo and double check your change is there.


# Image Processing and Tracking
This submit was from a branch.
# I want to work without worrying about messing up someone elses edits
Welcome my friend to branching!!!

So you want to develop a new feature(capability or code) but don't want people to mess with your edits or to mess with their edits. You want to be a team player and so you decide to learn branching and merging. 

Lets create a branch for your feature! Navigate on your terminal to the project repo and run the following
```
git branch WRITE-A-BRANCH-NAME
```
Please choose a good name - "JesusPleaseLetThisFeatureWorkWhenIMerge" is insufficient but I hope your prayers are accepted.

Now you have created a branch, lets see all the available branches.
```
git branch
```
You should see yours and other! Now lets switch to your branch. 
```
git checkout INSERT-YOUR-BRANCH-NAME    
```
A top tip is that when you write `git checkout` you can click *tab* to list the options you have and autocomplete the command by writing a couple letters of the option you want and hitting tab many times to feel pro.

OK - now command `git branch` again and you should see a `*` next to your branch. You can now go wild at your own risk, the wilder your code changes are the more likely you will have to deal with conflict resolution later on if it touches someone elses code. So maybe have a little chat with the person whose coding youre interfacing with.

Now you should edit the `README.md` file and commit those changes.
```
git add README.md
git commit -m "my first commit on my branch"
git push origin BRANCH-NAME
```
Awesome! If you run into errors I wish you best of luck with stackoverflow or feel free to contact me.

Navigate to the github page of the project and look for a drop down menu button called `main`. Then select your branch and you should see your changes! Also note how the main branch hasnt changed.
## Merging
For future reference run ` git fetch` to get the changes someone might of made to your branch(This is a very safe method that wont affect your code) then `git merge` to merge. You can do `git pull` but it will make decisions for you.

Lets merge your branch 

```
git checkout BRANCH
git merge main
```
Resolve conflicts you see and then 

```
git add .
git commit -m "what changes"
git push
```
Now go to the github repo and follow the instructions regarding the pull request. Leave detail comments wherever given the option. 
