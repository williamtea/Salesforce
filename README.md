# Salesforce

This is my first github creation, this will also be used to showcase some of the progression of Salesforce development that I've learned on my own spare time through Udemy.

The Course that I'm taking is called [The Complete Salesforce Development Course](https://www.udemy.com/course/salesforce-development/).

These are the subjects that I'll be learning.
<img src="Udemy - What you'll learn.PNG" />

The first thing I've learned was about Primative Data Types and how to create comments.

Below is the code that I created.
```apex
//A any set of characters surrounded by single quotes
String myName = ('William Tea');
System.debug(myName);
//Returns true or false or null
boolean doYouEnjoyCoding = true;
System.debug(doYouEnjoyCoding);
//Returns up to 32bit number (2,147,483,647)
Integer myAge = 26;
System.debug(myAge);
//Returns up to 64 bit number (2,147,483,648) followed by an L
Long myCellPhone = 8324756959L;
System.debug(myCellPhone);
//A number that includes a decimal point
Decimal myWeight = 179.4;
System.debug(myWeight);
//Returns up to 64 bit number that includes a decimal point
Double pi = 3.14159;
System.debug(pi);
//Returns a particular day
Date todayDate = Date.newInstance(2021, 08, 04);
System.debug(todayDate);
//A value that indicates a particular time
Time currentTime = Time.newInstance(21, 43, 0, 0);
System.debug(currentTime);
//A value that indicates particular day and time, such as a time stamp
Datetime currentDateTime = DateTime.newInstance(2021, 08, 04, 21, 43, 0);
System.debug(currentDateTime);
```

This was the output 
<img src="Primative Data Types.PNG" />
