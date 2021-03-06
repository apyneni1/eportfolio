## Welcome to Aparna Pyneni ePortfolio (Course ID:CS-499)!!!

### Professional Self-Assessment:

I am working as a software quality assurance professional from last 7 years and my goal is to become a software engineer. The overall computer science program and capstone project have broadened the understanding on software development life cycle phases – software requirements, design & architecture, development, security and quality etc. and deepened the expertise in multiple technologies such as Java, MySQL, HTML, XML, C, Android, C++, Python, Unix, GitHub and Mongo database etc. Below are some of the key soft skills and experiences gained through the course which prepared me well to work on the real-world software projects. 
- Strengthened collaboration and listening skills by partnering with rest of the class through discussion forums and email communications. 
- Improved planning and organizing skills by completing all the assignments and projects on time.
- Gained real-world software development experience by completing the projects mirroring real life examples. 

The computer science capstone course has brought all the learnings and experiences from the rest of program together to understand the end-to-end software development cycle broadly and deeply, and strengthen above listed skills further.  Below is the list of enhancements performed and skills polished through same.
1. Strengthened the software design and engineering skills by enhancing the complexity, security and capabilities of “Wellness Tracker” mobile application login and registration experiences.
2. Improved the algorithms and data structures skills by developing efficient and effective secure coding standards for an enterprise security policy.
3. Advanced the database skills by writing queries using complex SQL concepts such as LEFT JOIN, RIGHT JOIN and ALTER statements. 


### Code Review
Code review is one of the quality assurance activities in which one verifies the fellow programmer’s code systematically. The person performing the code review is called as reviewer and must not be the code’s author. It is also referred as peer review or inspection. Performed the code review by reading the source code and same can be accessed by [cliking here](https://drive.google.com/file/d/1mIsoqiwTEVkUQecCC-kZwE3un40CNizz/view?usp=sharing).

### Enhancement One: Software Design and Engineering
"Wellness Tracker" is an Android mobile application designed intutively for consumers to track daily weight and manage weight loss goals. Enhanced this app to improve the software design and engineering practices such as avoiding the duplicate usernames and increase the password criteria etc. Full write-up on the enhancements made can be accessed by [clicking here](https://github.com/apyneni1/eportfolio/blob/ad244e6d344d9ccd89ac993f19cf66e4af17e60a/3.2%20Milestone%20Two%20Narrative.pdf).

Following are the snippets of code enhancements and full code of before and after enhancements can be downloaded bellow. Android Studio software is required to execute the code.
- Pre-enhancements application code: [Download](https://github.com/apyneni1/eportfolio/blob/1f2b77cf1755eb4a038a75ef39bd2b577c5a637a/AparnaPyneni_WeightTracker.zip)
- Post-enhancements application code: [Download](https://github.com/apyneni1/eportfolio/blob/a757987cff2220bbb76ae319aa0331540909a3ec/MyApplication.zip) 

**Code from MainActivity class**
```
if (!uname.isEmpty()){
      boolean IsUsernameTaken = myDB.UsernameExists(uname);
      if (!IsUsernameTaken && !pwd.isEmpty() && pwd.length() >6) {
           boolean isInserted = myDB.insertUser(uname, pwd);
```
**Code from WeightTrackerDB class**
```
Cursor cur = db.query(WeightTables.TABLE1, columns, selection, selectionArgs, null, null, null);
int count = cur.getCount();
if(count > 0)
  return true;
else
  return false;
```
### Enhancement Two: Algorithms and Data Structure
Established enterprise security policy for Green Pace organization to produce the software securely and consistently. The security policy includes coding principles, code standards and vulnerabilities if not followed etc. This document is enhanced to include following three new coding standards of data structures and complete writeup of enhancements can be accessed by [clicking here](https://github.com/apyneni1/eportfolio/blob/7032ae9b470646b485a71bc900e549741eade7ef/4.2%20Narrative.pdf).

1. Always initialize pointers values to nullptr
2. Do not use pointer arithmetic on polymorphic objects
3. Pair the memory allocate and deallocate functions correctly.

**Compliance code example for the first newly added coding standard**
```
#include <new>
  
void f() {
  int *i1, *i2;
  try {
    i1 = new int;
    i2 = new int;
  } catch (std::bad_alloc &) {
    delete i1;
    delete i2;
  }
}
```
**Non-compliance code example for the first newly added coding standard**
```
#include <new>
  
void f() {
  int *i1 = nullptr, *i2 = nullptr;
  try {
    i1 = new int;
    i2 = new int;
  } catch (std::bad_alloc &) {
    delete i1;
    delete i2;
  }
}
```
All the secure coding standards are applicable for C and C++ software languages.
- Pre-enhancements security policy: [Download](https://github.com/apyneni1/eportfolio/blob/1f2b77cf1755eb4a038a75ef39bd2b577c5a637a/Security%20Policy_Pre_Enhancment.pdf)
- Post-enhancements security poliocy: [Download](https://github.com/apyneni1/eportfolio/blob/02150486618eddd57347301e61b3e324a867cbdd/4.2%20Security%20Policy.pdf) 

### Enhancement Three: Databases 
MySQL is an open-source relational database management system. I have enhanced the SQL queries to include advanced SQL concepts such as ALIAS, ALTER, COUNT, INNER JOIN, LEFT JOIN and RIGHT JOIN etc. In addition to these the SQL queries code includes data definition and modification statements like CREATE, INSERT, DELETE and UPDATE. The full narrative of SQL enhancement made can be accessed by [clicking here](https://github.com/apyneni1/eportfolio/blob/ad244e6d344d9ccd89ac993f19cf66e4af17e60a/5.2%20Narrative.pdf).

Following are the code samples of advanced SQL concepts. 

**Add new column to the table**
```
ALTER TABLE person 
 ADD gender VARCHAR(1) NOT NULL;
```
**LEFT JOIN SQL query**
```
select m.message_id as "Message ID",   
 m.message as "Message",
 m.send_datetime as "Message Timestamp",
 i.image_name as "First Image Name",
 i.image_location as "First Image Location"
 from message m
 Left join message_image ip on ip.message_id = m.message_id
 Left join image i on i.image_id = ip.image_id
 group by m.message_id;
```
- Pre-enhancements SQL queries code: [Download](https://github.com/apyneni1/eportfolio/blob/1f2b77cf1755eb4a038a75ef39bd2b577c5a637a/SQL%20queries_Pre_Enhancement.txt)
- Post-enhancements SQL queries code: [Download](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/queries.txt)

You need intall MySQL to execute the SQL query code.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
