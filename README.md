
This tutorial uses JBehave 3.x and Selenium 2.x to test [movietickets.com](http://movietickets.com)

<img src="http://jbehave.org/reference/preview/images/jbehave-logo.png" alt="JBehave logo" align="right" />

## Running the stories

This will run the build and (after a minute or so) Firefox will open and test the movietickets.com website:

    mvn clean install 

You should see Firefox (installed on your system) flicker as it tests movietickets.com

This will run a single story (one contained in a D0_1088.story file):

    mvn clean install -DstoryFilter=D0_1088

This will run a suite based on the meta filters in the three story files:

    mvn clean install -Dmeta.filter="+color red"

## Viewing the results

In directory target/jbehave/view, a page named 'reports.html' has been generated, which you open that in any browser to the stories that have run and their execution status.

There should be a row for each story.  The story reports are clickable to via links on the right-most column.

## Using this tutorial to start your own JBehave-based integration tests for a web site.

The tutorial aims to provide a fully-functional project that you can use to model you own project:

1. src/main/java/com/mtc/stories/MTCStories.java is the entry-point that JBehave uses to run the stories. 
2. src/main/stories contains the stories run by JBehave via MTCStories.java.
3. src/main/java/com/mtc/steps/MTCSteps.java contains the steps.
4. src/main/resources/mtc-steps.xml contains the Spring configuration for composition the steps.

To run the test on different browsers from commandline cd into the directory 
mvn clean install -Dbrowser="chrome"

By Default the test will run in firefox .

Other supported browsers please refer the below link 
http://jbehave.org/reference/web/stable/javadoc/web-selenium/org/jbehave/web/selenium/PropertyWebDriverProvider.html


