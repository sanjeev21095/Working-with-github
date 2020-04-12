It is useful to learn about Github by practicing with a project. Start by creating a local directory
```
mkdir my_new_git_project
cd my_new_git_project
git clone <insert link of a repository you want to clone>
```
What you have doen so far is cloned or made copies from the repository on the upstream repository (from where you copied the link to clone)
on to:  |
  1. Local Repository  
  2. Staging Area  
  3. Working Directory - Same as the directory where you create the project (In the above example, its my_new_git_project)  

<table class="tg">
  <tr>
    <th class="tg-7btt" colspan="3">Local</th>
    <th class="tg-c3ow"><span style="font-weight:bold">Remote</span></th>
  </tr>
  <tr>
    <td class="tg-0pky">Working Directory</td>
    <td class="tg-0pky">Staging Area</td>
    <td class="tg-0pky">Local Repositoy</td>
    <td class="tg-0pky">Upstream Repositry</td>
  </tr>
  <tr>
    <td class="tg-0lax" colspan="4">    <span style="font-weight:bold">&lt;-------------------------------Cloning-----------------------------------</span></td>
  </tr>
</table>

+  ``` git status``` tells how the files in the working directory are related to the files in other stages.  
 
Now, we can make changes that we eventually want to be synced with the upstream repository. But we do not want to do this 
until we are sure that these are final enough versions to share. We might have a lot of changes to make in the project to be uploaded
upstream. However, we really want to track only those changes that we feel are worth to keep a track of. Edits in the staging area 
are not kept by the version control system. We add a file to the staging area with the ```git add``` command.  






<table>
  <tr>
    <th colspan="3">Local</th>
    <th><span style="font-weight:bold">Remote</span></th>
  </tr>
  <tr>
    <td>Working Directory</td>
    <td>Staging Area</td>
    <td>Local Repositoy</td>
    <td>Upstream Repositry</td>
  </tr>
  <tr>
    <td colspan="2"><span style="font-weight:bold">--------------Add-------&gt;</span><br></td>
    <td></td>
    <td></td>
  </tr>
</table>
  
For example, consider 2 new text files that has the text "Test" and "Temporary". We want to add this to the staging area. What we need to do is:  
```
echo "Test" >> test_file.txt
echo "Temporary" >> temp_file.txt
git add test_file.txt
```
What you have done now is added the ```test_file``` to the staging area. You can now check the status with the ``` git status``` command.
You will see a different message stating there is a new file staged that has not been committed and you also have an untracked file. 
It is easy to recognize which files I am talking about now. So now, any changes we make to ```test_file``` will get added to 
the repository next time we commit.  
  
How do I commit?

<table>
  <tr>
    <th colspan="3">Local</th>
    <th><span style="font-weight:bold">Remote</span></th>
  </tr>
  <tr>
    <td>Working Directory</td>
    <td>Staging Area</td>
    <td>Local Repositoy</td>
    <td>Upstream Repositry</td>
  </tr>
  <tr>
    <td></td>
    <td colspan="2"><span style="font-weight:bold">---------Commit-----------&gt;</span></td>
    <td></td>
  </tr>
</table>

Let us add a new line to the ```test_file```.
```
echo "Adding a new line" >> test_file.txt
```
