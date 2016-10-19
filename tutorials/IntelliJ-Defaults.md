---
layout: essay
type: essay
title: IntelliJ Defaults
date: 2016-10-18
labels:
---

<h2>Introduction</h2>

Here's a way to reassign default settings for IntelliJ so it will work with our classes JavaScript Coding Standards.

<h2>Tutorial</h2>

<h3>1. Navigate to the Default Settings</h3>
Start up IntelliJ. At the bottom of the startup window, go to `Configure > Project Defaults > Settings`. If you're on Windows, there should be an option under `File>Other Settings>Default` Settings. 

<img class="ui huge floated image" href="../images/Tutorials/IntelliJ-Defaults/config1.png">

After this step you can just follow the steps outlined in the (JavaScript Coding Standards)[http://courses.ics.hawaii.edu/ics314f16/morea/coding-standards/reading-javascript-coding-standards.html] page.

<h3>2. Import and add the ics-se-code-style Code Style Scheme</h3>
Go to `Editor > Code Style > JavaScript`. Import the <a href="http://courses.ics.hawaii.edu/ics314f16/morea/development-environments/ics-se-code-style.xml" target="#"> ics-se-code-style.xml</a> into IntelliJ and select it.

<a href="../images/Tutorials/IntelliJ-Defaults/config2.png" target="#"><img class="ui huge floated image" href="../images/Tutorials/IntelliJ-Defaults/config2.png"></a>

Then make sure that it's the selected scheme. 

<a href="../images/Tutorials/IntelliJ-Defaults/config3.png" target="#"><img class="ui huge floated image" href="../images/Tutorials/IntelliJ-Defaults/config3.png"></a>


<h3>3. Enable ESLint</h3>

Go to `Languages & Frameworks > JavaScript > Code Quality Tools > ESLint`.

Select the files for the correct ESLint Package. I chose to keep a copy of the `.eslintrc` configuration file in my folder for this class so I don't need to add a new file each time. 

<a href="../images/Tutorials/IntelliJ-Defaults/config4.png" target="#"><img class="ui huge floated image" href="../images/Tutorials/IntelliJ-Defaults/config4.png"></a>


<h3>4. Turn off JavaScript Inspections</h3>

Go to `Editor > Inspections` and un-check JavaScript.

<a href="../images/Tutorials/IntelliJ-Defaults/config5.png" target="#"><img class="ui huge floated image" href="../images/Tutorials/IntelliJ-Defaults/config5.png"></a>


<h3>5. Define ECMAScript 6</h3>

Go to `Languages & Frameworks > JavaScript` and set the JavaScript language version to ECMAScript 6.

<a href="../images/Tutorials/IntelliJ-Defaults/config6.png" target="#"><img class="ui huge floated image" href="../images/Tutorials/IntelliJ-Defaults/config6.png"></a>

