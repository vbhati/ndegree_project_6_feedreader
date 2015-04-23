#### Project Overview

This project is a web-based application that reads RSS feeds. Jasmine is used to write a number of tests against a pre-existing application. These will test the underlying business logic of the application as well as the event handling and DOM manipulation.


#### Running application:

1. Clone the application on your system

2. Launch index.html in browser.

3. Below tests will get executed automatically and will list the results at the bottom of the page.


#### Test Specs implemented:

1. Write a test that loops through each feed in the allFeeds object and ensures it has a URL defined and that the URL is not empty.

-> Checks if url is "", '', null, undefined

2. Write a test that loops through each feed in the allFeeds object and ensures it has a name defined and that the name is not empty.

-> Checks if name is "", '', null, undefined

3. Write a test that ensures the menu element is hidden by default.

-> Menu will be hidden if class value of body element is "menu-hidden". Spec checks this value for validation

4. Write a test that ensures the menu changes visibility when the menu icon is clicked. This test should have two expectations: does the menu display when clicked and does it hide when clicked again.

-> This is implemented by invoking click event on menuicon and checking the class value of body item whether it is "menu-hidden" (means hide menu) or ""(means show menu)

5. Write a test that ensures when the loadFeed function is called and completes its work, there is at least a single .entry element within the .feed container.

-> This is implemented using "beforeEach" for asyncronous call and by checking length of .feed container childrens (.i.e .entry).

6. Write a test that ensures when a new feed is loaded by the loadFeed function that the content actually changes.

-> Passing index 1 to test above scenario which should load CSS feeds not Udacity feeds (default).
   Added setTimout to see it functioning. To make sure it actually changes contents I have used ".header-title" value.
   If content changes title changes vice versa.

 See feedreader.js for more details on implementation of above specs.