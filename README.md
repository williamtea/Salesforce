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

//Capitalize
System.debug('Capitalize myFirstName: '+ myFirstName.capitalize());

//Convert to upper case
System.debug('Changing first name to upper case: '+ myFirstName.toUpperCase());

//Convert to lower case
System.debug('Changing last name to lower case: '+ myLastName.toLowerCase());

//Equals
System.debug('Is my first name equal to Tea?: '+ myFirstName.equals('Tea'));
String myFirstName1 = 'William';
String myFirstName2 = 'william';
System.debug('myFirstName1 equals myFirstName2: '+ myFirstName1.equals(myFirstName2));
System.debug('myFirstName1 equals myFirstName2 ignore case: ' + myFirstName1.toLowerCase().equals(myFirstName2.toLowerCase()));

//Remove
System.debug('Remove last 3 characters of my first name: '+ myFirstName.remove('iam'));

// replace
System.debug('Replace my first name with Billy: '+ myFirstName.replace('william', 'Billy'));
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

The next exercise I've learned was about [List Datatypes](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/langCon_apex_collections_lists.htm).

Below is the code I created.
```apex
//Create a list
List<Integer> areaCode= new List<Integer>{713, 832};
System.debug('These are Houston\'s area codes' + areaCode);

//Add to the list
areaCode.add(346);
System.debug('These are the additional area codes' + areaCode);

//Get item on index 1
Integer areaCodeNum = areaCode.get(1);
System.debug('My cellphone number starts with ' + areaCode.get(1));

//Add item on index 2
areaCode.add(2, 281);
System.debug('These are even more area codes' + areaCode);

//Get the list size
System.debug('There are a total of ' + areaCode.size() + ' area codes in Houston.');

//Remove the item on index 3
areaCode.remove(3);
System.debug('These are the remaining area codes in Houston ' +areaCode);
System.debug('There is now total of ' + areaCode.size() + ' area codes left in Houston.');

//Clear the list
areaCode.clear();
System.debug('There are ' + areaCode + ' area codes stored.');
System.debug('There is a total of ' + areaCode.size() + ' area codes stored');
```

This was the code's output:

<img src="/images/List Data Types.PNG" />

The next exercise I've learned was about  [Set Datatypes](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/langCon_apex_collections_sets.htm).

Below is the code I created.
```apex
//Create a set
Set<Integer> areaCode = new Set<Integer>{713, 832, 346};
System.debug('These are Houston\'s area codes' + areaCode);

//Add to the list
areaCode.add(281);
System.debug('These are the additional area codes' + areaCode);

//Check if set has an item
System.debug(areaCode.contains(713));
System.debug(areaCode.contains(911));

//Delete an item
areaCode.remove(832);
System.debug(areaCode);

//Get set size
System.debug(areaCode.size());

//Check if set is empty
System.debug(areaCode.isEmpty());

//Remove all items
areaCode.clear();
System.debug(areaCode.isEmpty());
```

This was the code's output:

<img src="/images/Set Data Types.PNG" />

The next exercise I've learned was about  [Map Datatypes](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/langCon_apex_collections_maps.htm).

Below is the code I created.
```apex
Map<Integer, String> class2021 = new Map<Integer, String>();

//Add a new student/item
class2021.put(100001, 'William');
System.debug(class2021);

class2021.put(100002, 'Elaine');
class2021.put(100003, 'Tommy');
class2021.put(100004, 'Leo');
class2021.put(100005, 'Connie');
System.debug(class2021);

class2021.put(100005, 'Sarah');
System.debug(class2021);

//Update/override value
class2021.put(100005, 'Julie');
System.debug(class2021);

//Get a value
System.debug(class2021.get(100002));

//Remove an item from map
class2021.remove(100005);
System.debug(class2021);

//Get all the keys
Set<Integer> idNumber = class2021.keySet();
System.debug(idNumber);

//Get all the values
List<String> students = class2021.values();
System.debug(students);

//Check if map has the key
System.debug(class2021.containsKey(100001));
System.debug(class2021.containsKey(100005));
```

This was the code's output:

<img src="/images/Map Data Types.PNG" />

