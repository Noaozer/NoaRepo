---
id: 1kj71
title: "Sprint 7 - STD "
file_version: 1.1.2
app_version: 1.6.0
---

# **YOSSI**

1.  ticket #864e8dv54 - Onboarding improvements
*   change the intro screen

*   change UI placement for the interactive screens

*   change set up account page's blurred background - check the validation in set up account?

*   if users skip onboarding, add a new card to the homepage that triggers the videos again.

### what do you mean?

*   change set up account page's blurred background - check the validation in set up account?

*   📝 Make default step not in a loop ?

*   📝 Make IDE onboarding content taken from a different (deterministic) bucket ?

*   📝 Take the buttons names configurable from the Database ?

STD -

<br/>

|**Test Case Type**|**Description**                                           |**Test step**                                                                                                                                                                                                                                                                               |**Expected Result**                                                                                                                                                                                                                                                                                                                                                                                      |**Status** (Pass/Fail)|
|------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
|compatibility     |Intro screen - UI                                         |1.  compare UI to figma<br><br>    <br/><br><br/><br><br><br/>                                                                                                                                                                                                                              |1.  UI look as figma<br><br>    <br/><br><br/><br><br><br/><br><br><br/>                                                                                                                                                                                                                                                                                                                                 |<br/>                 |
|compatibility     |Wide screen adjustments                                   |1.  Open the login screen in laptop screen (14-16 inches)<br><br>2.  Open the login screen in standard screen size (24+ inches)<br><br>3.  Open the login screen in wide screen (X inches)                                                                                                  |1.  The intro screen adjusts itself to different screens size                                                                                                                                                                                                                                                                                                                                            |<br/>                 |
|Functionally      |Start tour - Interactive screens                          |1.  open intro screen<br><br>2.  click start tour butoon<br><br>3.  play every video in the interactive screens<br><br>4.  Click next and back in every interactive screen<br><br>    <br/><br><br/>                                                                                        |1.  starts the tour and transfers to the interactive screens<br><br>2.  the videos are displayed correctly, in order<br><br>3.  you can skip between the interactive screens (back/next)<br><br>4.  System theme - light<br><br>    <br/>                                                                                                                                                                |<br/>                 |
|Functionally      |Skip - interactive screens                                |1.  click Skip in every interactive screen<br><br>2.  set up your account<br><br>    <br/>                                                                                                                                                                                                  |1.  transfers from you to set up account page's blurred background<br><br>2.  'Start with a quick product tour' card appears in homepage that triggers the videos again<br><br>    <br/>                                                                                                                                                                                                                 |<br/>                 |
|Functionally      |Skip - Intro screen                                       |1.  click Skip in intro screen<br><br>2.  set up your account                                                                                                                                                                                                                               |1.  transfers to set up account page's blurred background<br><br>2.  'Start with a quick product tour' card appears in homepage that triggers the videos again                                                                                                                                                                                                                                           |<br/>                 |
|Functionally      |Set up account blurred background - light theme           |1.  set browser system theme light<br><br>2.  click Skip in intro \\interactive screen<br><br>3.  set up your account<br><br>    <br/>                                                                                                                                                      |1.  set up account blurred background is light                                                                                                                                                                                                                                                                                                                                                           |<br/>                 |
|Functionally      |Set up account blurred background - dark theme            |1.  set browser system theme dark<br><br>2.  click Skip in intro \\interactive screen<br><br>3.  set up your account<br><br>    <br/>                                                                                                                                                       |1.  set up account blurred background is dark                                                                                                                                                                                                                                                                                                                                                            |<br/>                 |
|Functionally      |On boarding tour through homepage<br><br><br/>            |1.  set your browser system theme - light<br><br>2.  finish on boarding tour<br><br>3.  set up account<br><br>4.  click - Start with a quick product tour<br><br>5.  play every video in the interactive screens<br><br>6.  Click next and back in every interactive screen<br><br>    <br/>|1.  'Start with a quick product tour' card appears in homepage that triggers the videos again<br><br>2.  the videos are displayed correctly, in order<br><br>3.  you can skip between the interactive screens (back/next)<br><br>4.  UI look as figma -<br><br>i. darkened background<br><br>ii. interactive screens in a different resolution<br><br>iii. System theme - light<br><br><br/><br><br><br/>|<br/>                 |
|Functionally      |On boarding tour through homepage - dark mode<br><br><br/>|1.  set your browser system theme - dark<br><br>2.  finish on boarding tour<br><br>3.  set up account<br><br>4.  click - Start with a quick product tour<br><br>5.  play every video in the interactive screens<br><br>6.  Click next and back in every interactive screen                  |1.  'Start with a quick product tour' card appears in homepage that triggers the videos again<br><br>2.  the videos are displayed correctly, in order<br><br>3.  you can skip between the interactive screens (back/next)<br><br>4.  UI look as figma -<br><br>i. darkened background<br><br>ii. interactive screens in a different resolution<br><br>iii. System theme - dark<br><br><br/><br><br><br/> |<br/>                 |

<br/>

2.  STD - 🏷️ Demo repo content improvements deployment

Deploy a new version of the content.

*   Change "todo" to "todo (demo)" - ﻿﻿ I'm not sure if this is something to be done on github enterprise or the DB..

*   remove "Feature Set" doc

*   remove "A quick intro about Swimm" doc

*   remove "About this demo repo" doc

    <br/>

<br/>

|**Test Case Type**|**Description**                                                                                                                       |**Test step**                                                                                         |**Expected Result**                                                                                                                                                                                                                                                                                    |**Status (Pass/Fail)**|
|------------------|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
|Validation        |Docs side bar - Repositories list<br><br>name "todo (demo)"                                                                           |1.  click on Docs in the sidebar<br><br>2.  Make sure the name of the repository is "todo (demo)"     |1.  The name of the repository is "todo (demo)"                                                                                                                                                                                                                                                        |<br/>                 |
|Validation        |"todo (demo)" repo<br><br>*   Ticket - Adding multiple snippets (simultaneously) pushes the page up and displays whitespace background|1.  click Docs in the sidebar<br><br>2.  click on "todo (demo)"<br><br>    <br/><br><br/><br><br><br/>|1.  the heading is "todo (demo)"<br><br>2.  the routing in the top bar is : workspace name/todo (demo)/ main<br><br>3.  there is 5 docs in the todo demo repo: Smart Text, Auto-Sync Magic, Live Snippets, IDE integration, Swimm Vs. other tools, and 1 playlist: Start Here<br><br>    <br/><br><br/>|<br/>                 |

<br/>

*   click up: Adding multiple snippets (simultaneously) pushes the page up and displays whitespace background

I reproduced the bug, attached video + console images

1.  from a long file (40+ code lines) add multiple snippets simultaneously, must add enough snippets in order to be able to scroll through the doc at least a page down!

2.  In the few seconds that the snippets are added to the document, a white background appears at the bottom of the document that can be scrolled seems like it's part of the page

3.  Only after the snippets are loaded by clicking on the doc the white screen it closes

should try to reproduce when generative AI is off

STD:

<br/>

|**Test Case Type**|**Description**                                                                                       |**Test step**                                                                                                                                                                                      |**Expected Result**                                                                                                                                                                                                                                                         |**Status**|
|------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
|Functionally      |Adding multiple snippets simultaneously                                                               |1.  in a blank doc add 3 snippets 20 lines each simultaneously<br><br>2.  scroll through the doc                                                                                                   |1.  3 snippets were added to the doc simultaneously<br><br>2.  The page does not move up and the background remains the same                                                                                                                                                |<br/>     |
|Functionally      |Adding multiple snippets simultaneously with different size<br><br>(enough sizes to be able to scroll)|1.  in a blank doc add 5+ snippets with different size simultaneously<br><br>2.  scroll through the doc<br><br>\*enough sizes to be able to scroll<br><br><br/>                                    |1.  5+ snippets with different size were added to the doc simultaneously<br><br>2.  The page does not move up and the background remains the same                                                                                                                           |<br/>     |
|Functionally      |Adding multiple snippets simultaneously at the top of the doc                                         |1.  add content to the doc<br><br>2.  place the cursor on the first line in the document<br><br>3.  add 3 snippets 20 lines each simultaneously<br><br>4.  scroll through the doc                  |1.  3 snippets were added to the top part of the doc simultaneously<br><br>2.  The document adjusts according to the changes and the content moves down<br><br>3.  The page does not move up and the background remains the same                                            |<br/>     |
|Functionally      |Adding multiple snippets simultaneously at the bottom of the doc                                      |1.  add content to the doc<br><br>2.  place the cursor on the last line in the document<br><br>3.  add 3 snippets 20 lines each simultaneously<br><br>4.  scroll through the doc<br><br>    <br/>  |1.  3 snippets were added to the bottom part of the doc simultaneously<br><br>2.  The document adjusts according to the changes and the content moves up<br><br>3.  The page does not move up and the background remains the same                                           |<br/>     |
|Functionally      |Adding multiple snippets simultaneously at the middle of the doc                                      |1.  add content to the doc<br><br>2.  place the cursor between 2 snippets in the document<br><br>3.  add 3 snippets 20 lines each simultaneously<br><br>4.  scroll through the doc<br><br>    <br/>|1.  3 snippets were added to the middle part of the doc simultaneously<br><br>2.  The document adjusts according to the changes and part of the content moves up and part of the content moves down<br><br>3.  The page does not move up and the background remains the same|<br/>     |

<br/>

2.  Ticket - gap between two snippets using the mouse is missing

STD:

<br/>

|**Test Case Type**             |**Description**|**Test step**|**Expected Result**|**Status (Pass/Fail)**|
|-------------------------------|---------------|-------------|-------------------|----------------------|
|functionally/Usability/Security|<br/>          |<br/>        |<br/>              |<br/>                 |
|<br/>                          |<br/>          |<br/>        |<br/>              |<br/>                 |
|<br/>                          |<br/>          |<br/>        |<br/>              |<br/>                 |
|<br/>                          |<br/>          |<br/>        |<br/>              |<br/>                 |
|<br/>                          |<br/>          |<br/>        |<br/>              |<br/>                 |
|<br/>                          |<br/>          |<br/>        |<br/>              |<br/>                 |

<br/>

*   Arrow overlaps beginning of blank cell's "Type /" placeholder in editor ?

*   Auth pages E2E - Tests to add ?

# **ASAF**

📝 Collapse snippet when dragged

1.  on start dragging ➝ collapse the snippet if it was expanded

2.  on end drag ➝ bring the snippet to the state it was before the drag (expanded/collapsed)

3.  do not collapse out-of-sync/outdated snippets. - Why? can we do Smooth transition between collapse and expanded?

STD -

<br/>

|**Test Case Type**|**Description**                              |**Test step**                                                                                                                                                                                                                                      |**Expected Result**                                                                                                                                                                                                                                                                                                                                              |**Status (Pass/Fail)**|
|------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
|Functionally      |drag&drop collapse snippet                   |1.  create snippets<br><br>2.  collapse the snippets<br><br>3.  drag one snippet<br><br>4.  drop the snippet on another line in the document                                                                                                       |1.  when dragging the snippet is remains collapsed<br><br>2.  when dragging all the snippets collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will remain collapsed<br><br>5.  all the snippets remain collapsed<br><br>    <br/>                                                |p                     |
|Functionally      |drag&drop expanded snippet                   |1.  create snippets<br><br>2.  Keep the snippets expanded<br><br>3.  drag on snippet<br><br>4.  drop the snippet on another line in the document<br><br>    <br/><br><br/>                                                                         |1.  Holding the hamburger menu the snippets collapsed<br><br>2.  On drag the snippets will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will expand<br><br>5.  all the snippets will expand<br><br>    <br/>                                                        |p                     |
|Functionally      |drag&drop expanded snippet + show more       |1.  create a snippet<br><br>2.  Keep the snippet expanded and expand the snippet by clicking Show more on both sides<br><br>3.  drag the snippet<br><br>4.  drop the snippet on another line in the document<br><br>    <br/>                      |1.  Holding the hamburger menu the expanded snippet + show more parts collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will expand without the show more parts                                                            |p                     |
|Functionally      |drag&drop to the top part of the doc         |1.  create a snippet at the end of the doc so that there is scrolling distance to the doc title<br><br>2.  Keep the snippet expanded and drag it to the top part of the doc<br><br>3.  drop the snippet on the first line in the document          |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly to the first line in the doc<br><br>4.  The snippet will be dropped in the first line and will expand<br><br>5.  The rest of the content in the document has moved down                                        |p                     |
|Functionally      |drag&drop to the bottom of the doc           |1.  create a snippet at the top of the doc so that there is scrolling distance to the bottom of the doc<br><br>2.  keep the snippet expanded and drag it to the bottom part of the doc<br><br>3.  drop the snippet on the last line in the document|1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly to the last line in the doc<br><br>4.  The snippet will be dropped in the last line and will expand<br><br>5.  The rest of the content in the document has moved up                                            |p                     |
|Functionally      |drag&drop between Swimm commands             |1.  create a snippet<br><br>2.  add Swimm commands to the doc (snippet, table, mermaid, images...)<br><br>3.  Keep the snippet expanded and drag it<br><br>4.  drop the snippet on another line in the document between the commands               |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue between the commands and will expand<br><br>5.  The content in the document will be updated accordingly                           |<br/>p                |
|Performance       |drag&drop long expanded snippet              |1.  create a long snippet<br><br>2.  Keep the snippet expanded and drag it<br><br>3.  drop the snippet on another line in the document<br><br>4.  Make sure the snippet expands in less than 10 seconds                                            |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will expand in less than 10 seconds<br><br>5.  The content in the document will be updated accordingly<br><br>    <br/>       |p<br/>                |
|Functionally      |drag&drop expanded snippet and commit changes|1.  create a snippet<br><br>2.  Keep the snippet expanded and drag it<br><br>3.  drop the snippet on another line in the document<br><br>4.  commit the changes                                                                                    |1.  Holding the hamburger menu the snippet collapsed<br><br>2.  On drag the snippet will be shown collapsed<br><br>3.  The snippet drags smoothly in the doc<br><br>4.  The snippet will be dropped in the line marked in blue and will expand<br><br>5.  The content in the document will be updated accordingly<br><br>6.  In view mode the snippet is expanded|<br/>p                |
|Functionally      |drag&drop outdated snippet                   |1.  drag outdated snippet<br><br>2.  drop the snippet on another line in the document<br><br>    <br/>                                                                                                                                             |1.  when dragging the snippet it remains expanded<br><br>2.  The snippet drags smoothly in the doc<br><br>3.  The snippet will be dropped in the line marked in blue and will remain expanded                                                                                                                                                                    |p<br/>                |
|Functionally      |drag&drop out-of-sync snippet                |1.  drag out-of-sync snippet<br><br>2.  drop the snippet on another line in the document                                                                                                                                                           |1.  when dragging the snippet it remains expanded<br><br>2.  The snippet drags smoothly in the doc<br><br>3.  The snippet will be dropped in the line marked in blue and will remain expanded                                                                                                                                                                    |<br/>p                |

<br/>

# **DANA**

1.  STD - 📁 Global tokens should support more languages (Kotlin, Scala) - 2d

    <br/>

#860q49bgd

2.  STD - 🐞 Playlist Top Down | Adding a doc in a playlist - 404

3.  STD - 🐞 Copy & Paste long files is too slow (Nadav)

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/1kj71).
