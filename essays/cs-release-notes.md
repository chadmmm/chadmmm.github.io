---
published: true
layout: essay
type: essay
title: CS Release Notes
date: 2017-01-15
labels:
  - Software Engineering
  - GitHub
  - Meteor
  - JavaScript
  - HTML/CSS
  - Semantic UI
  - Issue Driver Project Management
---

The purpose of this essay is to keep track of the release notes for each new version of the CS (Collaborative Study) app that I am currently developing. With each release of the app, I will update this essay with the release notes that detail my contributions to the project. I started this project in my software engineering class (ICS 314) at the University of Hawaii at Manoa in the fall of 2016 and I'm now continuing development on the app with my group. If you are interested in more than just release notes, you can learn more about my contributions by visiting [my project page](../projects/CollaborativeStudy) on this website or you can learn more about the project overall at its [GitHub page](https://collaborativestudy.github.io/).

## January 15, 2017
---
The focus of this release is to improve the overall usability of the app.

### New Features and Fixes
  - **Require first and last name**: Displaying only UH usernames can make it difficult to identify other users. Requiring a first and last name will make it easier for users to get to know each other.
  - **Fix FullCalendar Bug**: There was a bug where clicking on a date in the calendar would not always trigger the modal to create a new study session. The solution to the problem was to update jQuery to the latest version.
  - **Prevent creating sessions in the past**: Previously, users were able to create study sessions in the past.

### Challenges
  A feature that I was not able to successfully implement during this release was the feature to automatically remove study sessions that have already passed. I'm currently searching for a way to run functions on the server side instead of relying on a user's actions to prompt the cleaning.

### Plans for the next Release
  - **Sessions cards**: Currently, the sessions page displays sessions in the form of a table. In the next release, the table will be converted into cards for each study session.
  - **Sessions search case-insensitive**: Searching for sessions only works if the exact string is searched for.
  - **General search improvements**: Allow for searching by more than just course title and also potentially implement sort and filter options.