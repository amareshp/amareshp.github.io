---
layout: post
title: Creating your own TestNG Annotation
---
[TestNG](http://testng.org/doc/documentation-main.html "TestNG Documentation") has many Annotations like `@Test`, `@DataProvider`, `@BeforeTest`, `@AfterTest`, etc.

**In most cases, these Annotations will suffice the user's needs, but what if you need a specific runtime behavior for your tests and none of these Annotations offer that behavior?**

Well, you can write your own Annotation for that and have your Annotation processed at runtime like other TestNG Annotations.

Here is how you do it - 

* Create a basic maven project and add TestNG as a dependency.
* Create your Annotation
* Create your Listener
* Create a folder called META-INF\services in src\main\resources
* Create a file called org.testng.ITestNGListener in src\main\resources\META-INF\services
* Add the following line to this file - `com.amareshp.annotations.MyTestNGAnnotationListener`  - (Note: You may have to leave a blank line below this line).

_To see a complete example - fork the project - **https://github.com/amareshp/testng-examples**_

[Custom Annotation](https://github.com/amareshp/testng-examples/blob/master/src/main/java/com/amareshp/annotations/MyTestNGAnnotation.java)

[Listener](https://github.com/amareshp/testng-examples/blob/master/src/main/java/com/amareshp/annotations/MyTestNGAnnotationListener.java)
