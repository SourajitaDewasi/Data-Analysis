## Pattern Matching In Sql

Hello there. 👋

We all have faced situations where we remembered a part of the word or line but not entirely. This happens with analysts all the time and hence SQL has the perfect solution to this called **Pattern Matching** and today we are going to dive through it. So, let's begin!!!

- **LIKE:** It is used to search for a specific pattern in a column.
- **NOT LIKE:** It is used to search if the specific pattern is not matched in column.

1. **%**: Represents any sequence of 0 or more characters
2. **_**: Used to replace a single character

Let's see this with an example of Student Table.

**Student Table:**

![Screenshot 2022-08-20 123524.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1660979142492/zI2AMkqve.jpg align="left")


- **a%**  : Starting with 'a'
- **_a%** : Second letter is 'a'
- **%a_** : Second last letter is 'a'


**SQL Statements**
```
Q. RETRIEVE ALL THE STUDENT WHOSE NAME STARTS WITH 'R'
A. SELECT * FROM Student WHOSE Name LIKE 'R%';

Q. RETRIEVE THE NAMES OF THE STUDENTS WHO SECURED 4 DIGIT RANK
A. SELECT Name FROM Student WHERE Rank LIKE '_ _ _ _';
``` 

Now, the doubt is how you deal with data of percentages **'%'** or underscores **'_'**
So, we use escape character backslash **'\'**.

**SQL Statements**
```
Q. RETRIEVE ALL THE STUDENT WHOSE MARKS ARE HAVE '78%' AND EMAIL HAVE 'ab' 
FOLLOWED BY A SINGLE CHARACTER AND HAVE '@' IN IT.
A. SELECT Name FROM Student WHERE Marks LIKE '78\%' AND EMAIL LIKE 'abc\_%@%;

``` 
\ is backslash used as an escape character to avoid '%' being misinterpreted as wild character and a part of data. 

This is all about Pattern Matching in SQL. I will keep on writing about more such topics on Database Management System and SQL.

Thanks for reading! ❤️

Also connect with me on my socials:
[LinkedIn](https://www.linkedin.com/in/sourajita-dewasi-52b3b4193/), [Twitter](https://twitter.com/SourajitaD) or [Github](http://github.com/SourajitaDewasi)!