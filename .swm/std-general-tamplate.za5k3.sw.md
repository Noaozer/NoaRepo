---
id: za5k3
title: "STD - General Tamplate   "
file_version: 1.1.2
app_version: 1.5.0
---

STP (software test plan) to -

1.  Unit testing

2.  Component Testing

3.  Integration Testing

4.  E2E testing

<br/>

|### Test Case Type             |### Description                                |### Test step                |### Expected Result |### Status|
|-------------------------------|-----------------------------------------------|-----------------------------|--------------------|----------|
|functionally/Usability/Security|purpose of the test<br><br>explain the use case|1.  step one<br><br>2.  .....|what should happened|Pass/Fail |

<br/>

<br/>

Test Case Type -

*   Functionally testing

*   Usability testing

*   Security testing

*   Regression Testing

*   Performance Testing

    <br/>
<br/>

# **YOSSI**

1) ticket #864e8dv54 - Onboarding improvements

*   change the intro screen

*   change UI placement for the interactive screens

*   change set up account page's blurred background - check the validation in set up account?

*   if users skip onboarding, add a new card to the homepage that triggers the videos again.
<br/>

STD -

<br/>

|**Test Case Type**|**Description**                                                                  |**Test step**                                                                                                                                |**Expected Result**                                                                                                                                                                                                                          |**Status** (Pass/Fail)|
|------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
|compatibility     |Intro screen                                                                     |1.  compare UI to figma<br><br>2.  Open the login screen in wide screen and narrow screen<br><br>3.  click start tour button<br><br>    <br/>|1.  UI look as figma<br><br>2.  Make sure that the intro screen adjusts itself to a standard screen size (24+ inches) and a laptop screen (14-16 inches)<br><br>3.  starts the tour and transfers to the interactive screens<br><br>    <br/>|<br/>                 |
|Functionally      |Interactive screens                                                              |1.  play every video in the interactive screens<br><br>2.  Click next and back<br><br>    <br/>                                              |1.  the video will be<br><br>2.  make sure you can skip between the interactive screens                                                                                                                                                      |<br/>                 |
|Functionally      |Skip - interactive screens                                                       |1.  click Skip in every interactive screen<br><br>2.  set up your account<br><br>    <br/>                                                   |1.  transfers to set up account page's blurred background<br><br>2.  a new card will be added to the homepage that triggers the videos again                                                                                                 |<br/>                 |
|Functionally      |Skip - Intro screen                                                              |1.  click Skip in intro screen<br><br>2.  set up your account                                                                                |1.  transfers to set up account page's blurred background<br><br>2.  a new card will be added to the homepage that triggers the videos again                                                                                                 |<br/>                 |
|Functionally      |On boarding tour through homepage<br><br>Homepage start with a quick product tour|1.  Skip on boarding start tour<br><br>2.  set up your account<br><br>3.  click - Start with a quick product tour<br><br>    <br/>           |1.  transfers to set up account page's blurred background<br><br>2.  UI look as figma - darkened background and the interactive screens will be in a different resolution<br><br>    <br/><br><br/>                                          |<br/>                 |

<br/>

2) STD - 🏷️ Demo repo content improvements deployment

Deploy a new version of the content.

*   Change "todo" to "todo (demo)" - ﻿﻿ I'm not sure if this is something to be done on github enterprise or the DB..
*   remove "Feature Set" doc

*   remove "A quick intro about Swimm" doc

*   remove "About this demo repo" doc
<br/>

<br/>

|**Test Case Type**|**Description**                                                |**Test step**                                                                                     |**Expected Result**                                                                                                                                                                                                        |**Status (Pass/Fail)**|
|------------------|---------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
|Validation        |Docs side bar - Repositories list<br><br>name "todo (demo)"    |1.  click on Docs in the sidebar<br><br>2.  Make sure the name of the repository is "todo (demo)" |1.  The name of the repository is "todo (demo)"                                                                                                                                                                            |<br/>                 |
|Validation        |"todo (demo)" repo                                             |1.  click Docs in the sidebar<br><br>2.  click on "todo (demo)"<br><br/><br><br><br/><br><br><br/>|1.  the heading is "todo (demo)"<br><br>2.  the routing in the top bar is : workspace name/todo (demo)/ main<br><br>3.  there is 5 docs in the todo demo repo and 1 playlist: Start Here, Smart Text,<br><br/><br><br><br/>|<br/>                 |
|Validation        |<br/>                                                          |<br/>                                                                                             |<br/>                                                                                                                                                                                                                      |<br/>                 |
|Validation        |Enter demo repo - name - remove "Feature Set" doc              |<br/>                                                                                             |<br/>                                                                                                                                                                                                                      |<br/>                 |
|Validation        |search "Feature Set" doc                                       |<br/>                                                                                             |<br/>                                                                                                                                                                                                                      |<br/>                 |
|Validation        |Enter demo repo - name - remove "A quick intro about Swimm" doc|<br/>                                                                                             |<br/>                                                                                                                                                                                                                      |<br/>                 |
|Validation        |search "A quick intro about Swimm" doc                         |<br/>                                                                                             |<br/>                                                                                                                                                                                                                      |<br/>                 |
|Validation        |Enter demo repo - name - remove "About this demo repo" doc     |<br/>                                                                                             |<br/>                                                                                                                                                                                                                      |<br/>                 |
|Validation        |search "About this demo repo" doc                              |<br/>                                                                                             |<br/>                                                                                                                                                                                                                      |<br/>                 |
|Validation        |make sure there is 5 docs in the todo demo repo and 1 playlist |<br/>                                                                                             |<br/>                                                                                                                                                                                                                      |<br/>                 |

<br/>

3) Ticket - Adding multiple snippets (simultaneously) pushes the page up and displays whitespace background

*   click up:

step to reproduce:

1) add multiple snippets simultaneously.

i. **Must** add enough snippets in order to be able to scroll through the doc.

In the few seconds that the snippets are added to the document, a white background appears at the bottom of the document that can be scrolled

When the snippets are loaded by clicking on the white screen it closes

*   attached video + console images
<br/>

<br/>

# **ASAF**

📝 Collapse snippet when dragged

1.  on start dragging ➝ collapse the snippet if it was expanded

2.  on end drag ➝ bring the snippet to the state it was before the drag (expanded/collapsed)

3.  do not collapse out-of-sync/outdated snippets. - Why? can we do Smooth transition between collapse and expanded?

STD -

<br/>

|**Test Case Type**|**Description**                              |**Test step**                                                                                                                                                                                                                                      |**Expected Result**                                                                                                                                                                                                                                                                                                                                              |**Status (Pass/Fail)**|
|------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
|Functionally      |drag&drop collapse snippet                   |1.  create a snippet<br><br>2.  collapse the snippet<br><br>3.  drag the snippet<br><br>4.  drop the snippet on another line in the document                                                                                                       |1.  when dragging the snippet it remains collapsed<br><br>2.  The snippet drags smoothly in the doc<br><br>3.  The snippet will be dropped in the line marked in blue and will remain collapsed                                                                                                                                                                  |<br/>                 |
|Functionally      |drag&drop expanded snippet                   |1.  create a snippet<br><br>2.  Keep the snippet expanded and drag it<br><br>3.  drop the snippet on another line in the document<br><br/><br><br><br/>                                                                                            |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will expand<br><br/>                                                                                                          |<br/>                 |
|Functionally      |drag&drop expanded snippet + show more       |1.  create a snippet<br><br>2.  Keep the snippet expanded and expand the snippet by clicking Show more on both sides<br><br>3.  drag the snippet<br><br>4.  drop the snippet on another line in the document<br><br/>                              |1.  Holding the hamburger menu the expanded snippet + show more parts collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will expand without the show more parts                                                            |<br/>                 |
|Functionally      |drag&drop new snippet with generative AI     |1.  Create a snippet that can be described using AI<br><br>2.  Keep the snippet expanded and drag it<br><br>3.  drop the snippet                                                                                                                   |1.  when dragging the snippet the generative AI tool tip disappear<br><br>2.  dropping the snippet the generative AI tool tip will reappear<br><br/>                                                                                                                                                                                                             |<br/>                 |
|Functionally      |drag&drop to the top part of the doc         |1.  create a snippet at the end of the doc so that there is scrolling distance to the doc title<br><br>2.  Keep the snippet expanded and drag it to the top part of the doc<br><br>3.  drop the snippet on the first line in the document          |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly to the first line in the doc<br><br>4.  The snippet will be dropped in the first line and will expand<br><br>5.  The rest of the content in the document has moved down                                        |<br/>                 |
|Functionally      |drag&drop to the bottom of the doc           |1.  create a snippet at the top of the doc so that there is scrolling distance to the bottom of the doc<br><br>2.  keep the snippet expanded and drag it to the bottom part of the doc<br><br>3.  drop the snippet on the last line in the document|1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly to the last line in the doc<br><br>4.  The snippet will be dropped in the last line and will expand<br><br>5.  The rest of the content in the document has moved up                                            |<br/>                 |
|Functionally      |drag&drop between Swimm commands             |1.  create a snippet<br><br>2.  add Swimm commands to the doc (snippet, table, mermaid, images...)<br><br>3.  Keep the snippet expanded and drag it<br><br>4.  drop the snippet on another line in the document between the commands               |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue between the commands and will expand<br><br>5.  The content in the document will be updated accordingly                           |<br/>                 |
|Performance       |drag&drop long expanded snippet              |1.  create a long snippet<br><br>2.  Keep the snippet expanded and drag it<br><br>3.  drop the snippet on another line in the document<br><br>4.  Make sure the snippet expands in less than 10 seconds                                            |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will expand in less than 10 seconds<br><br>5.  The content in the document will be updated accordingly<br><br/>               |<br/>                 |
|Functionally      |drag&drop expanded snippet and commit changes|1.  create a snippet<br><br>2.  Keep the snippet expanded and drag it<br><br>3.  drop the snippet on another line in the document<br><br>4.  commit the changes                                                                                    |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will expand<br><br>5.  The content in the document will be updated accordingly<br><br>6.  In view mode the snippet is expanded|<br/>                 |
|Functionally      |drag&drop outdated snippet                   |1.  drag outdated snippet<br><br>2.  drop the snippet on another line in the document<br><br/>                                                                                                                                                     |1.  when dragging the snippet it remains expanded<br><br>2.  The snippet drags smoothly in the doc<br><br>3.  The snippet will be dropped in the line marked in blue and will remain expanded                                                                                                                                                                    |<br/>                 |
|Functionally      |drag&drop out-of-sync snippet                |1.  drag out-of-sync snippet<br><br>2.  drop the snippet on another line in the document                                                                                                                                                           |1.  when dragging the snippet it remains expanded<br><br>2.  The snippet drags smoothly in the doc<br><br>3.  The snippet will be dropped in the line marked in blue and will remain expanded                                                                                                                                                                    |<br/>                 |

<br/>

# **DANA**

STD - 📁 Global tokens should support more languages (Kotlin, Scala) - 2d

#860q49bgd

<br/>

<br/>

<br/>

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/za5k3).
