## Introduction
Our Team will do the following:  

##### `Task 1`
Create an issue for every tasks inside the **folder** `issues` so to keep track of the Project Milestone #3.  
  
##### **`Task 2`**
Create a new project board using the **Basic Kanban** template, containing following columns:
* *"To do":* with **all current issues** and **all teammates' self introduction** :D
* *"In Progress":* set with automation that a **new pull request** will be put into the column
* *"Done":* set with automation that **merged pull requests** and **closed issues** will be put into the column

##### `Task 3`
Set up a **file** `readme.md` which will be displayed when entering the repo with 3 headings:  **Introduction**, **Code**, and **Contributors**. Then type a short summary of all the tasks to be done by the team.

##### `Task 4`  
Update the web page: `https://csci3251-2020.github.io/project-team-d` by editing the **Contributors** part in `readme.md`. Use a *loop* to display all the information inside **each teammates' .md files**. 
The CSS style can be changed.

##### `Task 5`  
Check if:  
* all the issues are being **labelled** in the project
* pull requests are added in the Project's **proper columns**
* all teammates have included their **.md file** in **folder** `_stu` 

##### `Task 6`  
Write a simple C code in `code.c`. Then set up a **GitHub Action with a workflow** to run the C code. 
Use *`gcc code.c -o code;`* and *`./code`* to run the code. This action will deploy the code every time there is a push into the master branch.

##### `Task 7`  
Update the web page: `https://csci3251-2020.github.io/project-team-d` by doing the following:
* including the code from *`code.c`* to `readme.md` using **`include_relative`**
* highlight the code using C syntax highlighting *with markdown*, a **workflow status badge** for the code will appear
* the workflow name will be the **first line** in `.github/workflows/ccpp.yml`, rename the name as the team name **without any space**. 
* under the code snipplet, insert a resultant image *using markdown*.  

##### `Task 8` 
Promote the team repo by first including the last updated time of the repo using `site.time`.
Then go to the public repo of **`csci3251-2020.github.io`** in the CSCI3251-2020 organization. 
Finally, edit the file to add a link of the team and request for review from **@chuckjee**.

## Code
## Contributors
{% for stus in site.stu %}
<div style= "border-radius: 25px;
  border: 2px solid white;text-align:center;margin:20px">
  <img src="{{stus.image}}" style="align=20px">
  <p> @{{stus.user}} ({{ stus.name }})</p>
  <p><b>{{ stus.content | markdownify }}</b></p>
</div>
{% endfor %}

last update at site.time
