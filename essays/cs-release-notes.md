---
published: true
layout: essay
type: essay
title: CS Release Notes
date: 2017-02-01
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

## February 15, 2017
---

### New Features and Fixes
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
