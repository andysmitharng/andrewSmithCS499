# Andrew Smith ePortfolio

### Self-Assesment
```
     I have learned a lot as I worked through my Computer Science program. Some of my education came from course work, some of it came 
from working on  my own projects. When I first decided to major in Computer Science, I wasn’t really sure what I ultimately wanted 
to do. As I started to develop basic programs, work with databases, and create application on both the back and front end, I was 
able to develop an idea of my strengths, weaknesses, and interest. I found that using creative problem solving, through the backend 
development of applications, was what I enjoyed the most. Having spent most of my adult life in the military, adding in a team 
environment really allowed me to excel. By working with others, both in class and outside of it, I was able to increase my skill set 
in software design, databases, algorithms, and security. This all really came together while working with Amazon Web Services (AWS). 
I started a project with my brother that incorporated multiple AWS services, it required me to use Python to populate a relational 
database with information from user file uploads. The function was secured using AWS’s group permissions and security best 
practices. I was able to collaborate with another developer, utilizing all of the skills I had learned in my degree program, and 
create a secure solution to a problem.

     I have chosen 2 artifacts to represent my work in software design, databases, and algorithms. The first artifact is an Android 
application designed to allow a user to search for campgrounds based on name, city, or feature. They can also use location services to 
find camps near their location. The application has a user login that is secured using an MD5 hash and then it is securely stored on the 
company database. It also uses SQLite to store and query user data and campground information. Location services are only accessed with 
user permissions and there is social media integration through the ability to post campground experiences on Facebook. The second 
artifact is a program that loads in a file containing eBay bids run by a local government. The program allows a user to search the bids 
in order to do an audit. They can search by government department or by a specific bid. All of the data for each bid is stored in a 
binary search tree to make searching as fast as possible. The search tree uses nodes to store information and point to the next node. 
```

## Artifacts

#### Code Review
This code review reperesents my ability to create a present a presentation to a team. It is a review of some of my projects and their planned enhancements

[Code Review](https://bitbucket.org/andrew_smith13/code-review/downloads/)

#### Software Design and Databases

```
    For my Software Design/Engineering artifact I chose the Campsite Locator application that I created in CS-360 last term. The
application allows the user to search for campgrounds based on name, features, or city. It also allows them to find the camps on Google 
maps and post their experience to Facebook. I picked this artifact because it is a complete program that provides a value to the user.  
It has many design elements such as the GUI, databases, location services, and social media. The place it needed improvement was 
security, it has a login, but the login wasn’t very secure and used a text file in the phone to store credentials. Storing the 
credentials in the phone meant the user could only access the app from their phone. The username and password are now stored on a 
database, simulated as if stored on a company server. I also added an MD5 hash class to hash the user’s password before it is stored. 
This increases security by hashing the password and storing the credentials on a server instead on in the phone. It makes the app more 
functional by allowing the user to have access from any device.
    
	My improvements meet the course outcomes I had planned on, develop a security mindset and implement a solution to deliver value. 
Developing these enhancements were pretty straight forward. I already had the MD5 hashing algorithm from a previous course and the 
database was setup for the campsite search function. I did gain more insight into using SQLite in Java. I was able to create a more 
advanced query and then read back the response. My only hang up occurred when I ran the emulator, the add new user function worked, but 
the login crashed the application. After a lot of searching I was able to pull the DB file from the system and see that the login table 
wasn’t being created. I had to delete the file then restart the emulator, this fixed the problem, and everything ran smoothly from 
there.

     The database artifact I used was also from my Campsite Locator app. The database uses SQLite to store and query information about 
each campground. The app is designed to allow a user to search for campgrounds based on name, features, or city. The database was 
utilized to store the campground data in a table with id, name, features, and city columns. I chose this artifact because it not only 
shows my ability to utilize SQL queries, but to then iterate through the return and display it. Originally the user could only search by 
one category, and only one campground could be returned. This was done through a basic SQL, SELECT FROM WHERE, query and then a cursor 
is used to read in the first return line from the query. IF/ELSE statements were then used to determine which category was used for the 
search, then display the missing data. I updated the queries to allow for the use of multiple fields, a user can now put in a city and 
feature and get a return of a campground that matches their needs. This search can be done by combing any two fields. I also updated the 
display so that when just a city or just a feature is searched for, the top three matches will be displayed to the user.
	
     These enhancements have met the two course outcomes I had originally set, creating value and utilizing algorithms to solve a 
problem. The application is now more valuable to the user because they can find multiple campgrounds to meet their needs. They can also 
be more specific in their search criteria, which allows them to get results that specifically match their requirements. The searches use 
SQL queries to search the campground table, then algorithms to iterate through the raw database return and display it to the user in a 
useful manner. The biggest hurdle for me was figuring out how to display more than one campground. I ended up watching a lot of 
tutorials to learn how to use ListView. Once I had an idea of how ListView worked, I worked on using a cursor to read in the return then 
send it to my ListView activity for display to the user. Implementing the cursor was the hardest part and took a lot of trial and error. 
I now have a much better understanding of how to iterate through the SQLite query return and then 
send it to a different class to be displayed.

```

[Campsite Locator Application](https://bitbucket.org/andrew_smith13/androidapplication/downloads/)

#### Algorithms and Data Structures

```
     The Algorithms & Data Structures artifact I chose to use is binary search tree. It was created to allow someone to search a listing 
of eBay sales run by various departments in a local government.  The eBay sales are stored in a CSV file, it lists the item sold, 
auction ID, department that made the sale, sale price, and the government fund the money went into. I chose this artifact because it 
uses two different data structures and various algorithms to load, search, and display the sales. It has a data structure to store the 
sale information and a structure to create nodes utilized in a linked list. There are then two algorithms that load the sales into a 
binary search tree and a vector. The binary search tree is utilized to organize the sales bids by bid ID because the bid ID creates a 
unique key. This makes the binary search tree very efficient at searching for bids by ID. I then enhanced the program by adding a vector 
that is sorted by department. I chose a vector because it is easy to partition and alphabetize. The vector then allows the user to 
display all the sales done by a chosen department. I also improved the program by allowing the user to input search criteria directly 
into the console, it had previously only allowed search criteria to be entered as arguments into a command prompt.

	My improvements meet my course objectives of creating value and solving a given problem using algorithmic principles. It adds value 
to the user by allowing them to look at what each department is selling and how much they are making. This would be useful if these 
government departments were being inspected for compliance with any laws governing selling used government equipment. The value is added 
by using algorithms and data structures that make the program perform efficiently at each task. The biggest hurdle I had was coming up 
with a way to search for the sales by department. The binary search tree works great when searching for a unique identifier, but it does 
not work as well when the search key can have multiple outputs. Once I chose to use a vector to hold the data for the department search, 
everything else ran smoothly. It took me a while of trying to make the binary search tree perform both searches before I chose to switch 
to a vector. I learned to look at more than one approach, instead of just trying to make the one I had work. 
```

[Government Auction Audit Tool](https://bitbucket.org/andrew_smith13/ebay-search/downloads/)
