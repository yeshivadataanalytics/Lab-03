# Lab #3: Develop Code Repository and Push Commits 


**Points: 10 **
**Assignment Type: Group submissions**

### Description:

In this lab, we will learn how to develop a GitHub Repository, generate a repository for a series of  functions and push the changes to a GitHub Repository

You will split up into the same groups designated for your final projects and a submission will be a Repo as a package for each Group. 

The following outlines the structure of the lab: 


1. **GitHub:**
	1.1 clone repo 
	1.2 create and checkout a branch
	1.3 make and commit a change to readme.txt
	1.4 push your changes back to GitHub
	1.5 merge your changes on github.com

2. **script: download date from API and save to S3**
	2.1. open .ipynb in jupyter
	2.2 Updates
	2.3 save to S3


## 1. GitHub:
### 1.1 clone repo 

```bash
git clone <repo url>
```

GitHub desktop:
<kbd>
![clone](./img/gui-clone.png)
</kbd>

### 1.2 create and checkout a branch 

```bash
git checkout -b <new-branch>
```
<kbd>
![branch](./img/gui-commit.png)
</kbd>

### 1.3 make and commit a change to readme.txt

* **Modify the text in the  box below put a message to your group,**

```
adding above

looking a how to merge files 

and below

```
* Save the file
* Commit those changes 

```bash
git add . # add all files that have changes 
git status # see the changes that are staged
git commit -m "put your commit message here" # commit your changes with a message

```
<kbd>
![commit](./img/gui-commit.png)
</kbd>

### 1.4  Push your changes back to GitHub


```bash
git push -u origin <branchname> #push your changes to a new remote branch
```

<kbd>
![push](./img/gui-push.png)
</kbd>

### 1.6 Merge changes 

#### 1.6.1 Open a pull request on the repo www.github.com/jacoblgoodman/{repo}>
<kbd>
![pull request](./img/GitHub-pullrequest-newpr.png)
</kbd>


#### 1.6.2 select the branch that you pushed

<kbd>
![select branch](./img/GitHub-pullrequest-branch.png)
</kbd>


#### 1.6.3 resolve and conflicts

<kbd>
![conflicts](./img/GitHub-pullrequest-resolve.png)
</kbd>


#### 1.6.4 commit the merge and close the Pull Request

<kbd>
![commit](./img/GitHub-pullrequest-commit.png)
</kbd>
<br>
<b>Congratulations! You are now a GitHub collaborator!</b>


## 2. script: download date from API and save to S3:

Now that you have installed GitHub Desktop and collaborated on a piece of code, we are going to develop a basic API call to pull data from a web service and convert it into a file to be consumed into a database. 

To get started, take the steps necessary to create a repository for your Group. You should title it by the group names and add brandon.chiazza@gmail.com and jacoblgoodman@gmail.com as collaborators to those repositories. 

Upon initiating the GitHub Repo for your Group, create a readme.md file and add the names of the group members to the read me. 

Your result should look something like this: 
<kbd>
![ReadMe](./img/readme_lab.PNG)
</kbd>





| Response Code | Response                        | Reference                                     |
|---------------|---------------------------------|-----------------------------------------------|
| 100           | Continue                        | [RFC7231, Section   6.2.1]                    |
| 101           | Switching Protocols             | [RFC7231, Section   6.2.2]                    |
| 102           | Processing                      | [RFC2518]                                     |
| 103           | Early Hints                     | [RFC8297]                                     |
| 104-199       | Unassigned                      |                                               |
| 200           | OK                              | [RFC7231, Section   6.3.1]                    |
| 201           | Created                         | [RFC7231, Section   6.3.2]                    |
| 202           | Accepted                        | [RFC7231, Section   6.3.3]                    |
| 203           | Non-Authoritative Information   | [RFC7231, Section   6.3.4]                    |
| 204           | No Content                      | [RFC7231, Section   6.3.5]                    |
| 205           | Reset Content                   | [RFC7231, Section   6.3.6]                    |
| 206           | Partial Content                 | [RFC7233, Section   4.1]                      |
| 207           | Multi-Status                    | [RFC4918]                                     |
| 208           | Already Reported                | [RFC5842]                                     |
| 209-225       | Unassigned                      |                                               |
| 226           | IM Used                         | [RFC3229]                                     |
| 227-299       | Unassigned                      |                                               |
| 300           | Multiple Choices                | [RFC7231, Section   6.4.1]                    |
| 301           | Moved Permanently               | [RFC7231, Section   6.4.2]                    |
| 302           | Found                           | [RFC7231, Section   6.4.3]                    |
| 303           | See Other                       | [RFC7231, Section   6.4.4]                    |
| 304           | Not Modified                    | [RFC7232, Section   4.1]                      |
| 305           | Use Proxy                       | [RFC7231, Section   6.4.5]                    |
| 306           | (Unused)                        | [RFC7231, Section   6.4.6]                    |
| 307           | Temporary Redirect              | [RFC7231, Section   6.4.7]                    |
| 308           | Permanent Redirect              | [RFC7538]                                     |
| 309-399       | Unassigned                      |                                               |
| 400           | Bad Request                     | [RFC7231, Section   6.5.1]                    |
| 401           | Unauthorized                    | [RFC7235, Section   3.1]                      |
| 402           | Payment Required                | [RFC7231, Section   6.5.2]                    |
| 403           | Forbidden                       | [RFC7231, Section   6.5.3]                    |
| 404           | Not Found                       | [RFC7231, Section   6.5.4]                    |
| 405           | Method Not Allowed              | [RFC7231, Section   6.5.5]                    |
| 406           | Not Acceptable                  | [RFC7231, Section   6.5.6]                    |
| 407           | Proxy Authentication Required   | [RFC7235, Section   3.2]                      |
| 408           | Request Timeout                 | [RFC7231, Section   6.5.7]                    |
| 409           | Conflict                        | [RFC7231, Section   6.5.8]                    |
| 410           | Gone                            | [RFC7231, Section   6.5.9]                    |
| 411           | Length Required                 | [RFC7231, Section   6.5.10]                   |
| 412           | Precondition Failed             | [RFC7232, Section 4.2][RFC8144, Section 3.2]  |
| 413           | Payload Too Large               | [RFC7231, Section   6.5.11]                   |
| 414           | URI Too Long                    | [RFC7231, Section   6.5.12]                   |
| 415           | Unsupported Media Type          | [RFC7231, Section 6.5.13][RFC7694, Section 3] |
| 416           | Range Not Satisfiable           | [RFC7233, Section   4.4]                      |
| 417           | Expectation Failed              | [RFC7231, Section   6.5.14]                   |
| 418-420       | Unassigned                      |                                               |
| 421           | Misdirected Request             | [RFC7540, Section   9.1.2]                    |
| 422           | Unprocessable Entity            | [RFC4918]                                     |
| 423           | Locked                          | [RFC4918]                                     |
| 424           | Failed Dependency               | [RFC4918]                                     |
| 425           | Too Early                       | [RFC8470]                                     |
| 426           | Upgrade Required                | [RFC7231, Section   6.5.15]                   |
| 427           | Unassigned                      |                                               |
| 428           | Precondition Required           | [RFC6585]                                     |
| 429           | Too Many Requests               | [RFC6585]                                     |
| 430           | Unassigned                      |                                               |
| 431           | Request Header Fields Too Large | [RFC6585]                                     |
| 432-450       | Unassigned                      |                                               |
| 451           | Unavailable For Legal Reasons   | [RFC7725]                                     |
| 452-499       | Unassigned                      |                                               |
| 500           | Internal Server Error           | [RFC7231, Section   6.6.1]                    |
| 501           | Not Implemented                 | [RFC7231, Section   6.6.2]                    |
| 502           | Bad Gateway                     | [RFC7231, Section   6.6.3]                    |
| 503           | Service Unavailable             | [RFC7231, Section   6.6.4]                    |
| 504           | Gateway Timeout                 | [RFC7231, Section   6.6.5]                    |
| 505           | HTTP Version Not Supported      | [RFC7231, Section   6.6.6]                    |
| 506           | Variant Also Negotiates         | [RFC2295]                                     |
| 507           | Insufficient Storage            | [RFC4918]                                     |
| 508           | Loop Detected                   | [RFC5842]                                     |
| 509           | Unassigned                      |                                               |
| 510           | Not Extended                    | [RFC2774]                                     |
| 511           | Network Authentication Required | [RFC6585]                                     |
| 512-599       | Unassigned                      |                                               |
