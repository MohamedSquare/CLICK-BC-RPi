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