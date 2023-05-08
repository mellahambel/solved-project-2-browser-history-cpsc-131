Download Link: https://assignmentchef.com/product/solved-project-2-browser-history-cpsc-131
<br>
<span style="font-size: 2.61792em; letter-spacing: -1px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Introduction</span>

Modern browsers keep track of browsing history which allows users to recall previously visited web pages using the back arrow button. When a user navigates back to a previous web page, they also have the option to navigate forward in the navigation history using the forward arrow button. However, if the user navigates back to a previous page and then goes to a new web page, all web pages that previously could be accessed with the forward arrow button are discarded. This behavior is well suited for Linked Lists. In this project you will write C++ code to model this behavior.




For a good video overview of this, <u>​</u><a href="https://youtu.be/_jQhALI4ujg?t=7m10s">check out this link</a><u>​</u><a href="https://youtu.be/_jQhALI4ujg?t=7m10s">.</a>




In addition, when asked, your program should respond with every web page visited and when it was visited. Since we do not know how many sites the user will visit, we will have a second Linked List that will keep track of every site visited.




You are given a simple text file of a user’s browsing history containing their actions: ​<em>back</em>​, <em>forward</em>​, or ​<em>new</em>​. If their action is listed as ​<em>new</em>​, it will be followed with a web address. Simulate their browsing history based on this text file.




<h1>Objective</h1>

You are given partial implementations of two classes. <strong>Webpage​</strong>​      is a class that holds both the web page url as well as the time it was first visited. The time visited is the number of seconds from the UNIX epoch, 00:00 Jan 1, 1970 UTC. C++ has a variable type that can handle this, named time_t.




<strong>BrowserHistory​</strong> is where the bulk of your work will be done. <strong>BrowserHistory​</strong>​ stores both a linked list representation of the user’s navigation history, as well as an overall history of all sites they’ve visited. It will be able to read the history from a text file.




The text file will have 3 basic commands: new, back, and forward. Back and forward will simulate the user pressing the back and forward arrow buttons of their browser. New will be followed by the web page’s url and the time the site was visited.




You are to complete the implementations of these classes, adding public/private member variables and functions as needed.




<strong>You are encouraged to use the </strong><u>​</u><a href="http://www.cplusplus.com/reference/list/list/"><strong>C++ Standard Library containers</strong></a>​<strong> (such as std::list, and std::list::iterator) for this project.</strong>




Your code is tested in the provided <strong>main.cpp​</strong>​    .




<h1>Source Code Files</h1>

You are given “skeleton” code files with many blank areas. Your assignment is to fill in the missing parts so that the code is complete and works properly when tested.

<ul>

 <li><strong>h​</strong>: Stores both a web page’s url and the time it was visited.</li>

 <li><strong>h​</strong>: stores both the user’s navigation history as well as their full history of sites visited.</li>

</ul>

○    This class contains a method to read item information from a text file.

<ul>

 <li><strong>cpp​</strong>: The entry point to the application. The main() function will test the output of your functions. This is already completed but feel free to change it for your own testing (during grading we will use the original main file).</li>

</ul>




<ul>

 <li><strong>md​</strong> file. You <u>​must edit this file</u>​ to include the name and CSUF email address of each student in your group. Do this even if you are working by yourself. We need this information so that we can enter your grades into Titanium. For example, if your group includes students Ada Lovelace and Charles Babbage, your <strong>README.md​</strong>​ should be in this format:</li>

</ul>

Group members:

Ada Lovelace <u>​</u><u><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="204144414c4f56454c414345604353550e46554c4c4552544f4e0e454455">[email protected]</a></u>

Charles Babbage <u>​</u><u><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="e98a81889b858c9a8b888ba98a9a9cc78f9c85858c9b9d8687c78c8d9c">[email protected]</a></u>




<h1>Hints</h1>

Start by implementing the Webpage class, then the BrowserHistory class. It can be overwhelming working on the BrowserHistory class so start with the constructor, then the visitSite() function, then the back() and forward() functions.




Remember the BrowserHistory class will include two linked lists, one for the navigation history and one for the full history of every site visited. It will also need an iterator or pointer to point to a specific position in the linked list.




Iterators are very similar to pointers. Both iterators and pointers can be tricky. Make sure you’re keeping track of whether you’re talking about an address or the object at that address. Remember to use the <strong>-&gt;</strong>​ <strong>​</strong> operator!




<h1>Obtaining and submitting code</h1>

We will be using ​<a href="https://classroom.github.com/">GitHub Classroom</a><u>​</u> to distribute the skeleton code and collect your submissions. This requires you to have an account on ​<a href="https://github.com/">github.com</a>​. If you are having trouble look at the following:

<ol>

 <li>Read Understanding the GitHub Flow and Hello World at <u>​</u><a href="https://guides.github.com/">GitHub Guides</a>​.</li>

 <li>Read the instructions below for your chosen development environment.</li>

</ol>




Click the assignment link to fork your own copy of the skeleton code to your PC. One student from a group clicks on the link below and forms a new team. The ​<u>team name must begin with</u> <u>your section number</u><u>​</u> (e.g., 2-Brians-team). This student then invites his/her project partner as an “Outside collaborator” in the settings menu.




<u>Do not fork your repository to your personal github account</u>​. Your code should have a URL like

https://github.com/CSUF-CPSC-131-Fall2018/project1-2-brians-team, NOT https://github.com/brian/project1-2-brians-team.

<a href="https://classroom.github.com/g/OqgM3v5p">https://classroom.github.com/g/OqgM3v5p</a>




(If you get an error when clicking the assignment link, chances are that your repository was still created successfully. Check your github.com page and you will see you are a member of the CSUF-CPSC-131-Fall2018 organization)




Here is a video that shows the steps: ​<a href="https://www.youtube.com/watch?v=-52quDR2QSc">https://www.youtube.com/watch?v=-52quDR2QSc</a> Then edit your code locally as you develop it. As you make progress, commit and push your changes to your repository regularly. This ensures that your work is backed up, and that you will receive credit for making a submission. Don’t wait until the deadline to learn how to push code!




<h1>Development environment</h1>

The test platform is Linux with the g++ -std=c++14 compiler. For this reason, the recommended development platform is Linux.

<h1>Linux development environment</h1>

To attempt to compile the test program, use the following command:

<strong>$ clang++ -g -std=c++14 *.cpp -o test</strong>




To attempt to run the compiled test program, use the following command: <strong>$ ./test</strong>




<h1>Automated Testing</h1>

We are also piloting the use of a continuous integration web service that automatically tests your code and gives real-time feedback. This service is provided courtesy of ​<a href="https://travis-ci.com/">Travis CI</a><u>​</u><a href="https://travis-ci.com/">.</a>




The Travis service will wait for you to push code to GitHub. After you do, it will try to compile and build your code. It will then send you an email describing the outcome. The email also has a link to a dashboard web page you can view to see a detailed log of what worked, or didn’t. This way you can get immediate objective feedback about how well your code is working. We recommend pushing your code to GitHub every time you reach a milestone and would like feedback on your progress.




You can check the results of automatic testing on Travis at ​<a href="https://travis-ci.com/">https://travis-ci.com/</a><u>​</u> (same login as your github account).


