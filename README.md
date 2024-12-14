# Instagram User Analyitcs


## Project Description

User analysis is the process by which we track how users engage and interact with our digital product (software or mobile application) in an attempt to derive business insights for marketing, product & development teams.
These insights are then used by teams across the business to launch a new marketing campaign, decide on features to build for an app, track the success of the app by measuring user engagement and improve the experience altogether while helping the business grow.
You are working with the product team of Instagram and the product manager has asked you to provide insights on the questions asked by the management team.


## Contents of the project includes answering the following questions:
### 1. Marketing
The marketing team wants to launch some campaigns, and they need your help with the following

### • Rewarding Most Loyal Users: 
People who have been using the platform for the longest time.
### Our Task: 
Find the 5 oldest users of the Instagram from the database provided

**Aim**: Find the 5 oldest users of the Instagram from the database provided.

**Approach**: 
1.We will be using our users table for this task and find out the oldest five users in it.
2.To find the users first sort the date column (created_at) in ascending order and limit its value to 5, so that it only displays five entries/ users.

**Command**

![Picture1](https://github.com/user-attachments/assets/b8f3a427-5d45-456a-a6e5-236b30282e65)

**The Result**

![Picture2](https://github.com/user-attachments/assets/78ef5b97-9010-4742-854b-5240fea6644d)

### • Remind Inactive Users to Start Posting: 
By sending them promotional emails to post their 1st photo.
### Our Task: 
Find the users who have never posted a single photo on Instagram

**Aim**: Find the users who have never posted a single photo on Instagram

**Approach**: 
1.Taking two tables into consideration ie; users and photos.
2.Will left join table photos with table users because both has a common field of id.
3.Finding rows from table where photo.id is NULL.

**Command**
![Picture3](https://github.com/user-attachments/assets/f10b56b7-35ea-4e48-a067-3e74cb963006)

**Result**
![Picture4](https://github.com/user-attachments/assets/7b775d39-6c61-4681-a188-893dd91c8bf4)

### • Declaring Contest Winner: 
The team started a contest and the user who gets the most likes on a single photo will win the contest now they wish to declare the winner.
###Our Task: 
Identify the winner of the contest and provide their details to the team

**Aim**: Identify the winner of the contest and provide their details to the team

**Approach**:
1.Selecting users.username, photos.id, photos.image_url, count(*) as TOTAL
2.Inner join all the three tables ie; users, photos, likes on likes,photo_id=photos.id and photos.id=users.id
3.Sort the data on the basis of TOTAL in descending order using the ORDER BY function.
4.Using LIMIT as 1 to find one most like photo will give us the winner of the contest.

**Command**
![Picture5](https://github.com/user-attachments/assets/ad48d942-0894-4665-8819-11f42b4c4662)

**Result**
![Picture6](https://github.com/user-attachments/assets/fe595f79-d056-4a20-9d2a-3e79935970e5)

### • Hashtag Researching: 
A partner brand wants to know, which hashtags to use in the post to reach the most people on the platform.
### Our Task: 
Identify and suggest the top 5 most commonly used hashtags on the platform

**Aim**: Identify and suggest the top 5 most commonly used hashtags on the platform

**Approach**:
1.Select tag_name and count(*) as TOTAL to show total number of tags from the tags table and join tags and photos table because both tables contains id as common field which has same values.
2.Using GROUP BY function, group the desired output and then using ORDER BY function, we can sort the output in descending order on the basis of TOTAL.
3.Using the LIMIT function, we can show only 5 required values for the task.

**Command**
![Picture7](https://github.com/user-attachments/assets/1b168ca7-56cf-4971-86c9-0f542dd8d26b)

**Result**
![Picture8](https://github.com/user-attachments/assets/64ed4327-689a-4565-a61c-1a2c94ba9343)

### • Launch AD Campaign: 
The team wants to know, which day would be the best day to launch ADs.
### Our Task: 
What day of the week do most users register on? Provide insights on when to schedule an ad campaign

**Aim**: What day of the week do most users register on? Provide insights on when to schedule an ad campaign

**Approach**:
1.Select dayname(created_at) and count(*) as total_users_registered from the users table.
2.Using GROUP BY function, we group data on the basis of day_of_week and by using ORDER BY we sort table on the basis of total_users_registered.

**Command**
![Picture9](https://github.com/user-attachments/assets/cf5c7f23-9baf-446c-b899-cd295eb943bc)

**Result**
![Picture10](https://github.com/user-attachments/assets/484c32e4-e17a-4cda-acf6-2d069fb2cf53)
