# NYU-Course-Buddy

An academic project for Cloud Computing (CS-GY-9233) at NYU Tandon with Prof Sambit Sahu.

NYU Course Buddy is a serverless web-app cum platform designed to help NYU students in the course registration process.

## Project Description and Motivation:

Every NYU student can relate with the struggle of registering for their desired classes. Often courses are full within seconds, leaving students grappling for courses they don’t wish to take. At the end, it is up to these students to find others who are interested in swapping the particular pair of courses they have with the ones they want. Another way students can register for a course is when someone else drops it. But the challenge is finding out when a course has become available. The students have to look at quite a few different places to find reviews about the subjects as well. The existing tools out there, i.e. Coursicle, RateMyProfessor, etc offer some relief but at a cost and are not consolidated as one solution. 

### Existing Products:
- [Coursicle](https://www.coursicle.com/)
- [NYU Albert](http://albert.nyu.edu/albert_index.html?tab=NYU_STUDENTS_TAB)
- [RateMyProfessor](https://www.ratemyprofessors.com/)

## Product Features:

We propose a web application that facilities our NYU students in the class registration process. It will have the following features:
1. A complete list of all the courses being offered for the current semester.
2. Ability to add courses to the user’s wishlist.
3. When a course that is in the wishlist becomes available, a notification will be sent to the user's email.
4. Ability to view and add new reviews/ratings for a particular course.
5. A dashboard for a high level view on course trends. For example, live charts/analytics for hot subjects and course ratings.
6. A smart chatbot through which users can query for various use cases like Open Courses, Trending Courses, etc 


## Data Source:

[Schedge](https://blog.torchnyu.com/2020/01/15/schedge-an-albert-api.html) - Albert course listing API

"Schedge is a program that scrapes Albert, then provides a simple API for course data. You can query course data from different semesters with all the corresponding meeting times and recitations."

## Architecture:

![Architecture](https://github.com/therealbappi/NYU-Course-Buddy/blob/main/Resources/System-Architecture.png?raw=true)

For design and prototype using Figma [click here](https://www.figma.com/proto/mXqgsQ9RWYtaqv3WDAT3eA/Cloud?node-id=0%3A1&scaling=min-zoom&starting-point-node-id=1%3A52)

1. AWS Services
2. Hosting on S3
3. User Authentication and Security using Cognito and IAM
4. APIs on API Gateway
5. Backend for APIs on Lambda
6. Master Databases: RDS 
7. Indexing on ElasticSearch
8. Chatbot on Lex
9. Notifications Emails using SES
10. Notification server on EventBridge + Lambda 
11. Queue user notifications with SQS

![notif_service](https://user-images.githubusercontent.com/26039974/169601631-a9d46fbf-b1bb-4d0f-82d4-0ed085c641bc.PNG)

![chatbot_service](https://user-images.githubusercontent.com/26039974/169601650-c87ed5e0-3f66-4716-b588-3ce3a60c5d42.PNG)

## Contributors:

Bharath Sai Reddy Chinthapanti (bc3177@nyu.edu)

Purva Kondaji (pk2312@nyu.edu)

Syed Ahmad Taqi (st4324@nyu.edu)

Viha Gupta (vg2237@nyu.edu)
