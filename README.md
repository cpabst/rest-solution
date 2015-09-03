# rest-solution

This is the README file for assignment to build a simple RESTful, JSON API for a note taking application.

I decided to implement the API in Java, using the [Spark](http://sparkjava.com/) web framework (NOT to be confused with the Apache Spark project :) ). The file `rest-test-0.0.1-SNAPSHOT-jar-with-dependencies.jar` is the compiled code and dependencies to run the web server hosting the API. The command to start the server (issued in the same directoery of the jar file) is

```javascript
java -cp rest-test-0.0.1-SNAPSHOT-jar-with-dependencies.jar com.cpabst.RestTest
```

The server runs on port **4567**, so hopefully you have nothing running on that port already.

I implemented all of the functionality listed in the Guidelines. Please see what you think. I have also uploaded the source code for my solution. It is in the ZIP file `RestTest_chris_pabst.src.zip`. This is a valid Eclipse project file if that makes your life easier (Luna).

Answers to your questions:

* How well does your note-searching-api scale or not scale? How would you make your search more efficient?

The index search should already scale well since I used a HashMap to save the data in memory. The text search will not scale as well due to the fact that every note would need to be scanned to find all matches. I would look for an opensource solution to assist in that, like [Lucene](https://lucene.apache.org/).

* How would you add security to your API?

I am not too familiar with RESTful security options, as wedidn't use any while I worked in REST. I would take a look at Spring security, as well as an OAuth 2 implementation like [Apache Oltu](https://oltu.apache.org/).

* What features should we add to this API next?

Since I do not persist the notes in my implementation, that would be the obvious next step to me. Maybe using [Derby](https://db.apache.org/derby/) (light) or [MySQL](https://www.mysql.com/) (heavy).

* How would you test the API? 

I would start with writing unit tests around each of the methods in RestTest (using JUnit) to verify the functionality during the test phase of the Maven build.

Chris Pabst
9/3/2015

