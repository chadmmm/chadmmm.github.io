---
published: true
layout: essay
type: essay
title: CS Release Notes
date: 2017-04-01
labels:
  - Software Engineering
  - GitHub
  - Meteor
  - JavaScript
  - HTML/CSS
  - Semantic UI
  - Issue Driver Project Management
---

The purpose of this essay is to keep track of the release notes for each new version of the CS (Collaborative Study) app that I am currently developing. With each release of the app, I will update this essay with the release notes that detail my contributions to the project. I started this project in my software engineering class (ICS 314) at the University of Hawaii at Manoa in the Fall of 2016 and I'm now continuing development on the app with my group. If you are interested in more than just release notes, you can learn more about my contributions by visiting [my project page](../projects/CollaborativeStudy) on this website or you can learn more about the project overall at its [GitHub project page](https://collaborativestudy.github.io/).

## April 1, 2017
---

My group is planning on conducting our usability test during the next release period, so I worked on eliminating any bugs that we could find in the app. Previously, the `user-profile-detail-page` was only displaying fake information no matter what user's profile was being viewed. I fixed this by having the page pull relevant information from the `Users` and the `Reviews` collections.

I also worked on figuring out a hosting solution to make the usability testing easier. By having our app hosted, it will prevent any bugs that are platform specific that exist on the server side. I currently have the app hosted on an extra computer that I have, but I am still trying to figure out the best configurations to ensure decent performance and security.

Group posts are now sorted with the newest posts listed on the top.

### Challenges

Most of the challenges that I have encountered so far while working on this project have not been directly me having difficulties in understanding how to apply what I've learned. Instead, the source of most of my challenges has been myself. In the past few weeks, I have been struggling with time management as my other classes have also been demanding a lot of my time. This past week was spring break for me and I feel like I was able to get more work done, but I still feel like I could have done more.

I feel like it's the right thing to take a short break from coding to conduct the usability test so I can get outside opinions on the app, and hopefully, it will help me to become inspired and more motivated.

### Plans for the next release (April 15, 2017)

The first part of the release period will be focused on conducting our usability test. Ideally, we will be able to conduct multiple usability tests with time to fix issues that we find between the tests. Depending on how well the usability tests go, I will have more or less time to work on fixing the issues.

## March 15, 2017
---

I spent a large amount of my time working on improving the calendar and scheduling features based on what I learned from working on `meteor-example-fullcalendar`. The modal for creating a study session previously used a raised segment container, which did not make a lot of sense. I modified the modal content to be in a Semantic UI container and I added CSS to create padding on the edges to the global stylesheet. All of the CSS for the calendar was also moved from the HTML file into the global stylesheet to make it easier to change color schemes, layouts, etc. The modal id was also changed from `#calendar` to `#create-study-session-modal` to prevent it from being confused with the actual calendar. The template that contained the content for the modal was also renamed from `Create_Study_Session_Page` to `Create_Study_Session_Modal`. There were also a few problems that were fixed with the form validation related to creating study sessions where not all of the fields were correctly validated. A new feature to the calendar is the ability to reschedule events by dragging and dropping them to different days.

Searching for sessions just got easier with the new sort feature that allows sessions to be sorted by their date so you can see what study sessions are coming up soon.

Reviews are also working now, which means that almost all of the basic functionality required to use the CS app is complete. The only feature that is left to be completed is the `User_Profile_Detail_Page`, which serves as a public profile that is visible to other users of the site.

### Challenges

Like in the last release, time management has been an issue for me. I probably could have accomplished more during this release period, but I wanted to focus on doing a thorough job of cleaning up the calendar. Part of the reason that the code for the calendar begin so messy was because it was rushed and I didn't question myself enough about whether each line was truly needed for the sake of having a functional calendar and study session scheduling system.

### Plans for next release (April 1, 2017)

Just because most of the required features have been implemented, that does not mean the end of development for the CS app. There's still a lot of other new features planned to improve the usability of the app. It's hard to know what features should be implemented to make our app easier to use because as developers, we have an idea in our mind of how the app should be used, but that does not necessarily match with how other people may be inclined to use the app. Because of this, our team has decided to conduct a usability test to get feedback. Most of the planning for the usability test has already been completed, but some bugs have already been found. This next release period will be dedicated to fixing any bugs that would prevent us from conducting the usability test and actually conducting the test.


## March 1, 2017
---

This release period was different from the previous release periods. Instead of working on the CS project, I dedicated my time to working on an example of integrating an interactive calendar with Meteor. This example is meant to be used by Software Engineering I students (ICS 314), at UH Manoa to gain a clearer understanding of how to implement a calendar with Meteor. When I took Software Engineering I, many of my peers and myself found it difficult to integrate a calendar. Having a simplified example to build on is something that I wish I had and that is the reason why I decided to work on one.

While working on the calendar example, I was able to find many improvements that could also be made to the calendar used by the CS app. Simplifying the calendar for the example made things easier to understand and I found that there was a lot of extra code that was not needed.

### Challenges

The largest challenge that I had during this release period was time management. These past two weeks for me have been full of assignments from all of my classes. I found it difficult to distribute time across all of my classes and my progress on the Meteor calendar example suffered as a result. I also had problems configuring ESLint to lint my project's JavaScript files, which took up a lot of the available time.

### Plans for next release (March 15, 2017)

I plan to finish up the Meteor Calendar Example during the early parts of this release period. After finishing up the example, I will continue where I left off with the plans that were previously scheduled for the March 1st release.

## February 15, 2017
---

### New Features and Fixes
  This release was focused mostly on bug fixes and design improvements.
  - **Sort courses on my page**: Courses on a user's homepage now appear in alphanumeric order.
  - **Profile picture bug fixed**: Profile pictures are being generated from URLs again.
  - **Edit group bug fixed**: Group members are no longer deleted when modifying group information.
  - **Tutorial toggle**: The toggle to enable/disable tutorials was moved from the

### Challenges
  Time management was definitely a challenge. During this release period, I spent a large amount of time working on implementing sort options when searching for a study session. I had to first decide whether the study sessions should be sorted on the server or on the client side and then I was having trouble collecting the data in a way that would make it sortable. Unfortunately, I was not able to successfully implement the feature during this release. Since I spent a significant amount of time on the sorting, I decided to move on to work on other issues.

### Plans for next release (March 1, 2017)
  Not many of the planned features and fixes were able to be completed during this release period, so they have been moved to the next period.
  - **User Bio improvements**: Allow users to include more information on their bios and add ability to edit bio.
  - **Notifications**: Receive notifications about upcoming sessions that you're signed up for, group invitations, etc.
  - **Search Improvements**: Implement sort options when searching for study sessions.
  - **Group visibility**: Allow group visibility to be set to public or private.
  - **Delete groups**: Add the option to delete a group.
  - **Homepage Redesign**: The homepage will be redesigned to be more inviting and simpler.
  - **User Bio improvements**: Allow users to include more information on their bios and add ability to edit bio.
  - **Fix Star Ratings**: Fix rounding errors when calculating a user's average rating.
  - **Admin rights**: Add the ability for admin rights to be assigned to a user/developer.
  - **Reviews unique to user**: Connect reviews to a specific user.


## February 1, 2017
---

### New Features and Fixes
  - **Convert Sessions table into cards**: Previously, a table was used to display all of the upcoming study sessions. Now, each session is represented by a clickable card that contains the title of the study session, course, and start/end times. Users can click on the card to get more detailed information about the study session.
  - **Group functionality**: The Groups feature is now functional. Groups can be created, users can be added/removed from groups, and group study sessions can now be created through invitations.
  - **Study session search improvements**: Study sessions can now be searched by course, title, or topic. Each of these fields are case-insensitive and can be searched by typing partial parts of the field. Look out for more even more search improvements in the next release!

### Challenges
  The main challenge for this release period was implementing search improvements. Before working on the search feature, I was not familiar with regular expressions, so I spent a large amount of time learning how to use them to improve the search features. Now that I have learned the basics of regular expressions, I will hopefully be able to further improve the search functionality before the next release.

  Another challenge was deciding on what features users of the site will be interested in and the best way to implement them as far as usability is concerned. A usability test will be planned for the future in order to get feedback on the app.

### Plans for the next release (February 15, 2017)
  - **User Bio improvements**: Allow users to include more information on their bios and add ability to edit bio.
  - **Additional settings**: Create a preferences menu to manage user settings across the site.
  - **Notifications**: Receive notifications about upcoming sessions that you're signed up for, group invitations, etc.
  - **Group visibility**: Allow group visibility to be set to public or private.
  - **Delete groups**: Add the option to delete a group.
  - **Group posts**: Group members will be able to post in groups to communicate with fellow group members.
  - **Study session search improvements**: There will be further improvements for searching study sessions.
  - **Fix profile picture**: For some reason, profile pictures are no longer being generated from URLs. This will be fixed.

## January 15, 2017
---
The focus of this release is to improve the overall usability of the app.

### New Features and Fixes
  - **Require first and last name**: Displaying only UH usernames can make it difficult to identify other users. Requiring a first and last name will make it easier for users to get to know each other.
  - **Fix FullCalendar Bug**: There was a bug where clicking on a date in the calendar would not always trigger the modal to create a new study session. The solution to the problem was to update jQuery to the latest version.
  - **Prevent creating sessions in the past**: Previously, users were able to create study sessions in the past.

### Challenges
  A feature that I was not able to successfully implement during this release was the feature to automatically remove study sessions that have already passed. I'm currently searching for a way to run functions on the server side instead of relying on a user's actions to prompt the cleaning.

### Plans for the next release (February 1, 2017)
  - **Sessions cards**: Currently, the sessions page displays sessions in the form of a table. In the next release, the table will be converted into cards for each study session.
  - **Sessions search case-insensitive**: Searching for sessions only works if the exact string is searched for.
  - **General search improvements**: Allow for searching by more than just course title and also potentially implement sort and filter options.
