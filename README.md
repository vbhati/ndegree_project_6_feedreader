#### Project Overview

This project is about writing test suites and specs using Jasmine for a preexisting web application that reads RSS feeds. These tests will test the underlying business logic of the application as well as the event handling and DOM manipulation.


#### Running application:

1. Clone the application on your system

2. Launch index.html in browser.

3. Below tests will get executed automatically and will list the results at the bottom of the page.


#### Test scenarios and Specs implementation:

##### Write a test that loops through each feed in the allFeeds object and ensures it has a URL defined and that the URL is not empty.

Spec Implementation : Checks if url is "", '', null, undefined

##### Write a test that loops through each feed in the allFeeds object and ensures it has a name defined and that the name is not empty.

Spec Implementation : Checks if name is "", '', null, undefined

##### Write a test that ensures the menu element is hidden by default.

Spec Implementation : Menu will be hidden if class value of body element is "menu-hidden". Spec checks this value for validation

##### Write a test that ensures the menu changes visibility when the menu icon is clicked. This test should have two expectations: does the menu display when clicked and does it hide when clicked again.

Spec Implementation : This is implemented by invoking click event on menuicon and checking the class value of body item whether it is "menu-hidden" (means hide menu) or ""(means show menu)

##### Write a test that ensures when the loadFeed function is called and completes its work, there is at least a single .entry element within the .feed container.

Spec Implementation : This is implemented using "beforeEach" for asyncronous call and by checking length of .feed container childrens (.i.e .entry).

##### Write a test that ensures when a new feed is loaded by the loadFeed function that the content actually changes.

Spec Implementation : Passing index 1 to test above scenario which should load CSS feeds not Udacity feeds (default). Added setTimout to see it functioning. To make sure it actually changes contents I have used ".header-title" value. If content changes title changes vice versa.

See feedreader.js for more details on implementation of above specs.