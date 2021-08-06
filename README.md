# Salesforce Developer Journey

This is my first github creation, this will also be used to showcase some of the progression of Salesforce development that I've learned on my own spare time through Udemy.

The Course that I'm taking is called [The Complete Salesforce Development Course](https://www.udemy.com/course/salesforce-development/).

These are the subjects that I'll be learning.
<img src="/images/Udemy - What you'll learn.PNG" />

I am going to learn about the Apex fundamentals, the first thing I've learned was about [Primative Data Types](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/langCon_apex_primitives.htm) and how to create [comments](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/langCon_apex_expressions_comments.htm).

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

This was the code's output:

<img src="/images/Primative Data Types.PNG" />

The next exercise I've learned was about the different [string class methods](https://developer.salesforce.com/docs/atlas.en-us.apexref.meta/apexref/apex_methods_system_string.htm).

Below is the code I created.
```apex
String myFirstName= 'william';
System.debug('Actual first name:' + myFirstName);

String myLastName= 'Tea';
System.debug('Actual last name:' + myLastName);

// capitalize
System.debug('Capitalize myFirstName: '+myFirstName.capitalize());

// convert to upper case
System.debug('Changing first name to upper case: '+myFirstName.toUpperCase());

// convert to lower case
System.debug('Changing last name to lower case: '+myLastName.toLowerCase());

// equals
System.debug('Is my first name equal to Tea?: '+myFirstName.equals('Tea'));
String myFirstName1 = 'William';
String myFirstName2 = 'william';
System.debug('myFirstName1 equals myFirstName2: '+ myFirstName1.equals(myFirstName2));
System.debug('myFirstName1 equals myFirstName2 ignore case: ' + myFirstName1.toLowerCase().equals(myFirstName2.toLowerCase()));

// remove
System.debug('Remove last 3 characters of my first name: '+myFirstName.remove('iam'));

// replace
System.debug('Replace my first name with Billy: '+myFirstName.replace('william', 'Billy'));
```

This was the code's output:

<img src="/images/String Class Methods.PNG" />

The next exercise I've learned was about the different [Escape Sequences](https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_select_quotedstringescapes.htm).

Below is the code I created.
```apex
//Escape Sequences demonstrating how to use apostrophes in a string along with returning to the next line 
String str = 'My future job title name\'s called a \'Application Support Developer\'. working at Sunnova Energy.\n the recruiter\'s name is Sri Gunukula.';
System.debug(str);
```

This was the code's output:

<img src="/images/Escape Sequence.PNG" />

The next exercise I've learned was about the different [List Datatypes](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/langCon_apex_collections_lists.htm).

Below is the code I created.
```apex
//Create a list
List<Integer> areaCode= new List<Integer>{713, 832};
System.debug('These are Houston\'s area codes' + areaCode);
//Add to the list
areaCode.add(346);
System.debug('These are the addtional area codes' + areaCode);
// get item on index 1
Integer areaCodeNum = areaCode.get(1);
System.debug('My cellphone number starts with ' + areaCode.get(1));
// add item on index 2
areaCode.add(2, 281);
System.debug('These are even more area codes' + areaCode);
// get the list size
System.debug('There are a total of ' + areaCode.size() + ' area codes in Houston.');
// remove the item on index 3
areaCode.remove(3);
System.debug('These are the remaining area codes in Houston ' +areaCode);
System.debug('There is now total of ' + areaCode.size() + ' area codes left in Houston.');
// clear the list
areaCode.clear();
System.debug('There are ' + areaCode + ' area codes stored.');
System.debug('There is a total of ' + areaCode.size() + ' area codes stored');
```

This was the code's output:

<img src="/images/List Datatypes.PNG" />

