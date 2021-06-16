## Welcome to Aparna Pyneni ePortfolio (Course ID:CS-499)!!!

### Professional Self-Assessment:

This section will be updated next week 

### Enhancement One: Software Design and Engineering
"Wellness Tracker" is an Android mobile application designed intutively for consumers to track daily weight and manage weight loss goals. Enhanced this app to improve the software design and engineering practices such as avoiding the duplicate usernames and increase the password criteria etc. Full write-up on the enhancements made can be accessed by [clicking here](https://github.com/apyneni1/eportfolio/blob/ad244e6d344d9ccd89ac993f19cf66e4af17e60a/3.2%20Milestone%20Two%20Narrative.pdf).

Following are the code enhancement snippets and full code can be downloaded by [clicking here](https://github.com/apyneni1/eportfolio/blob/a757987cff2220bbb76ae319aa0331540909a3ec/MyApplication.zip). You need to install Android Studio software to execute the application code.

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
Established enterprise security policy for Green Pace organization to produce the software securely and consistently. The security policy includes coding principles, code standards and vulnerabilities if not followed etc. This document is enhanced to include following three new coding standards of data structures and complete writeup of enhancements can be accessed by [clicking here](https://github.com/apyneni1/eportfolio/blob/ad244e6d344d9ccd89ac993f19cf66e4af17e60a/4.2%20Narrative.pdf).

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

[Full security policy](https://github.com/apyneni1/eportfolio/blob/7032ae9b470646b485a71bc900e549741eade7ef/4.2%20Narrative.pdf) document with 10 coding principles and 13 coding standards can be downloaded from here. All the secure coding standards are applicable for C and C++ software languages.

### Enhancement Three: Databases 
MySQL is an open-source relational database management system. I have enhanced the SQL queries to include advanced SQL concepts such as ALIAS, ALTER, COUNT, INNER JOIN, LEFT JOIN and RIGHT JOIN etc. In addition to these the SQL queries code includes data definition and modification statements like CREATE, INSERT, DELETE and UPDATE. The full narrative of SQL enhancement made can be accessed by [clicking here](https://github.com/apyneni1/eportfolio/blob/ad244e6d344d9ccd89ac993f19cf66e4af17e60a/5.2%20Narrative.pdf).

Following are the code samples of advanced SQL concepts. Complete list of [SQL queries](https://github.com/apyneni1/eportfolio/blob/c70ee92988776833762da71fe52d827f55c3b973/queries.txt) can be downloaded from here. You need intall MySQL to execute the SQL query code.

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
### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
