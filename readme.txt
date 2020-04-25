


{| style="border-spacing:0;width:7.4583in;"
|- style="border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;"
|| '''Lab '''
|| <nowiki>#3</nowiki>
|- style="border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;"
|| '''Points:'''
|| 10
|- style="border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;"
|| '''Assignment Type:'''
|| Group submissions
|- style="border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;"
|| '''Date Due:'''
|| 12/4 5:40 PM 


|-
|}

{| style="border-spacing:0;width:7.4931in;"
|-
| style="border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;" | First Name:
| style="background-color:#f2f2f2;border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;" | 
|-
| style="border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;" | Last Name:
| style="background-color:#f2f2f2;border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;" | 
|-
| style="border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;" | Student ID:
| style="background-color:#f2f2f2;border:0.5pt solid #000000;padding-top:0in;padding-bottom:0in;padding-left:0.075in;padding-right:0.075in;" | 


|-
|}
== Lab #3: Develop Code Repository and Push Commits  ==

== 0.0 Description ==

In this lab, we will learn how to develop a GitHub Repository, generate a repository for a series of Lambda functions and push the changes to a GitHub Repository


You will split up into the same groups designated for your final projects and a submission will occur as a package for each Group. 


* '''Group 1''': Natan Beinstock, Wen Chen, Qinghao Xia
* '''Group 2''': Jacob Goodman, Qihua Zhu, Jeeho Bae





The following outlines the structure of the lab: # Create GitHub Repo and Add Team for Lab
# Create web-scraper to load csv file into S3 Bucket
# Run and update web-scraper to iterate through all records stored on the Charities Bureau Website



== Create GitHub Branch and Repo and Add Team (2 pts.)  ==

In this portion of the lab, you will create a GitHub branch to manage your code across your group. You should nominate * Step 1. Use your GitHub account to create a new branch and repository and input the relevant code. 
** Step 1.1 Title the branch after your group and the lab (e.g., “Group_1_Lab_03”)
* Step 2. Enable for cloning for your team and have each team member clone repository to their local GitHub instance
* Step 3. Create a READ_ME.mcd file for this project
* Step 4. Copy the link to the repo and give [mailto:brandonchiazza@gmail.com brandonchiazza@gmail.com] permissions. Share it as part of your response to this lab'''. '''





Once you have completed this portion of the lab save your output files in a zipped packaged and send them to [mailto:brandon.chiazza@yu.edu brandon.chiazza@yu.edu]. You should send one per group. Your file name should look like: <<Group_Name>>_Lab_3_Submission_1

== Create web-scraper to load csv file into S3 Bucket (4 pts.) ==

''Note: there are dependencies. You will need to configure and install awscli and boto3 and be sure you give access to an S3 bucket. You can find documentation [https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html here]. Additional modules required include csv, pandas, dataframe, selenium, BeautifulSoup''. 

For this portion of the lab, we will be creating a web scraper to parse a table from the [https://www.charitiesnys.com/RegistrySearch/search_charities.jsp Charities Bureau Website]. From the website: ''“<span style="background-color:#ffffff;color:#05182a;">All charitable organizations operating in New York State are required by law to register and file annual financial reports with the Attorney General's Office. This includes any organization that conducts charitable activities, holds property that is used for charitable purposes, or solicits financial or other contributions.”''</span>

<span style="background-color:#ffffff;color:#05182a;">The site will contain vendor information and you are being tasked with culling a list into a csv file by scraping the website using the selenium module in Python. </span>

<span style="background-color:#ffffff;color:#05182a;">To begin take the following steps:</span>* Step 1. Load the script, scrape-to-csv-local.py, to your repository
* Step 2. Inspect the script, update the output file directory, and attempt to run the script. Become familiar with the Charities Bureau Website that is being scraped. 
* Step 3. Test the file locally
* Step 4. Once this works, commit the updated file to the repository (nominate one person to do this and another to peer review!)
* Step 3. Produce the csv output and ensure that the data from the dataframe exported appropriately
* Step 4. Save the file and take a screenshot of the directory that the file was saved to.



Variant: load the file into an s3 bucket* Step 1. Load the script, scrape-to-s3.py into your repository as a separate file
* Step 2. Create an s3 bucket to store your outputs of csv files. Note: I used a bucket named ‘database-update-bucket’. Be sure to make the settings on the s3 buckets public. As part of configuration of the awscli, you should ensure that you have access to s3 and the AWS environment. 
* Step 3. Update the scrape-to-s3.py file to include your s3 path
* Step 4. Test the file by inspecting the output on the s3 bucket
* Step 5. Once the test has passed, commit the changes to the master branch of your GitHub repository
* Step 6. Note that the output of the file has an issue! The header inserts a blank row! Update the script to remove the blank row in the csv output file
* Step 7. Test the file by inspecting the output on the s3 bucket
* Step 8. Once the test has passed, commit the changes to the master branch of your GitHub repository
* Step 9. Provide evidence that the file and script were successfully updated by providing the link to s3 and the .py file in the repository. 



Be sure to update your READ_ME.md file to reflect the script actions and ensure proper documentation.

Once you have completed this portion of the lab save your output files in a zipped packaged and send them to [mailto:brandon.chiazza@yu.edu brandon.chiazza@yu.edu]. You should send one per group. Your file name should look like: <<Group_Name>>_Lab_3_Submission_2


== Update web-scraper to iterate all results and load csv file into S3 Bucket (4 pts.) ==

For this portion of the lab, you should do this outside of class and with your team. You are going to alter the script, ''scrape-to-s3.py,'' to iterate through the pagination that exists on the page and compile all of the results in one dataframe from each page. Once you have done that, you should follow the same procedures in (2) to load the full csv file into the s3 bucket. 

Once the test has passed, commit the changes to the master branch of your GitHub repository. Provide evidence that the file and script were successfully updated by providing the link to s3 file and the .py file in the repository.


<div style="text-align:center;">[[Image:Picture 2.png|top]]</div>

Once you have completed this portion of the lab save your output files in a zipped packaged and send them to [mailto:brandon.chiazza@yu.edu brandon.chiazza@yu.edu]. You should send one per group. Your file name should look like: <<Group_Name>>_Lab_3_Submission_3

== BONUS: Use (3) to create a lambda function to run on a schedule to generate any updates from Charities Bureau Website. (5 pts.) ==

To earn extra points, you can compile your webscraping code into a zipped package and create the crawler in a lambda function to run on a schedule and run updates to the data file. From there, see if you can load the data into a simple MySQL RDS instance. The Python script should be able to accommodate all. 
