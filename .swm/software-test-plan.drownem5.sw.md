---
id: drownem5
title: Software Test Plan
file_version: 1.1.3
app_version: 1.12.1
---

**QA Enterprises - Git providers**  

**Intro**

*   The tests are designed to ensure the quality

*   The tests are divided into test subjects, at the end of each session bugs will be opened accordingly

*   Each test topic will contain all types of tests

    <br/>

**Q&A for the meeting;**

1.  Is there going to be any UI changes?

<br/>

<div align="center"><img src="https://firebasestorage.googleapis.com/v0/b/swimm-dev-content/o/repositories%2FZ2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI%3D%2F58434177-acbc-4f93-ae84-048aaa082980.png?alt=media&token=57184b4c-18fd-43b3-9a7e-0583e253c04b" style="width:'25%'"/></div>

<br/>

<div align="center"><img src="https://firebasestorage.googleapis.com/v0/b/swimm-dev-content/o/repositories%2FZ2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI%3D%2Ff8c96450-a190-4b76-8082-b11f6088dd77.png?alt=media&token=dc09146c-a390-43ae-9a6f-ba83744064ae" style="width:'25%'"/></div>

<br/>

1.  Do we implement Github App for the providers? and is it required testing? and how?

2.  Is the number of workspace users important?

3.  \*\*Auth\*\*  

    <br/>

**Points for the meeting:**

*   Orbit Sprint 14 (Go over sprint planning, testing time)

*   Work process definition

*   Bug handling (Ping Pong/ Step by step)

*   If you have any use cases or edge cases that you are thinking about, forward them to me

    <br/>

**Preconditions**

*   Explanation about the git provider - Git Lab, Bitbucket, Azure Devops (in details) 

*   Setting up a testing environment after development is complete and training before starting tests

*   Comprehensive testing plan - STP, and STD

    <br/>

**Testing Environment**

*   Dev local/Staging

*   Variable workspaces

*   Several repositories

    <br/>

**Testing strateg**

*   Performing QA tests in a continuous interface with the development team (Orbit) and fixing bugs on an ongoing basis

*   Regression - 2nd QA round
1.  After QA testing session and the bug fixes an additional session will be conducted that will include regression testing in order to make sure that fixing a bug did not create a new bug

2.  The tests will be written later according to the results of the first round

    <br/>

**Deadlines**

*   Release version bitbucket - **7.8** 

*   Release version Git Lab, Azure Devops - **1.9**

    <br/>

**Test Schedule**

*   Estimated times -

*   Testing -

*   Bug fixes -

    <br/>

**Software Test Plan:** 

Test Types:

1.  Sanity

2.  Functionality

3.  Performence

4.  Compatibility

5.  Multiple participants (?)

6.  Stress tests

Test Topics:

1.  New Users

2.  Authorize Git 

3.  Add Repo 

4.  General Repo Page tests

5.  Doc Life Cycle

6.  Sidebar

<br/>

|**Test Topic**         |**STP**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|New Users              |*   Create workspace (with X as git hosting)<br><br>*   UI changes<br><br>*   Set up account modal:<br><br>\*Git hosting platform<br><br>*   No Authorize Git messages<br><br>*   Create first doc and connect your repo through commit hub modal<br><br>*   Connect repository modal:<br><br>\*Select from all repositories<br><br>\*Select from public repositories<br><br>\*Allow Git provider Access<br><br>\*Security and SOC 2 review - Opens a page with customized content<br><br>Workspace page:<br><br>*   No authorization requested from user<br><br>*   Dummy repo exists on workspace - GitHub host<br><br>    <br/>                                                                                                                                                                                                                                                                                                                                                             |
|Authorize Git          |Exist Users:<br><br>*   Authorize Git request to every sign out and sign in<br><br>*   Validation for all buttons:<br><br>\***Authorization required** To access code-coupled content, make sure to authorize GitProvider first. [Learn more](https://docs.swimm.io/new-to-swimm/documentation-as-code)<br><br>\*Side bar **Authorization required button**<br><br>\*Create button disabled<br><br>\*create docs&playlist disabled - Don't show a number<br><br>\*Add repo disabled - Don't show a number<br><br>\*Add new - Sidebar<br><br>\*Search<br><br>*   Authorization performance - From the moment of clicking until loading the workspace<br><br>*   Measuring times for loading documents from the repo<br><br>*   Performance test for updating from the provider:<br><br>\*merged pr<br><br>\*changing code and documents that are outdated (snippets, tokens, path)<br><br>\*loading snippet studio<br><br>*   User settings - Integrate Github app<br><br>*   Re-authorize Swimm|
|Add Repo               |*   Add a repo<br><br>*   Connect repository modal<br><br>*   Repos loading time<br><br>*   Find repository<br><br>*   Mange Scope<br><br>*   Security and SOC 2 review - Opens a page with customized content<br><br>*   Add the same repo twice<br><br>*   Adding a repo that contains Swimm documents<br><br>*   Add a private repo that already exists in another workspace<br><br>*   Add a repo that returns an error message<br><br>    <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|General Repo Page tests|*   Create hub modal<br><br>*   Open on Git providers<br><br>*   Switch between repos<br><br>*   Loading documents<br><br>*   Deleting documents<br><br>*   Switch branch<br><br>*   Create a **new branch** and start a pull request<br><br>    <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|Doc Life Cycle         |*   Create Blank doc<br><br>*   Create Draft<br><br>*   Discard draft<br><br>*   Create hub modal<br><br>*   Commit the doc<br><br>*   Load Committed doc - View mode<br><br>*   Load Committed doc - Edit mode<br><br>*   Load an existing doc or draft<br><br>*   Export the doc to MD<br><br>*   Delete doc<br><br>*   Add snippets/tokens/path<br><br>*   Create PR<br><br>    <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|Sidebar                |*   Switch between repos<br><br>*   Loading documents<br><br>*   Adding a repo<br><br>*   Deleting a repo<br><br>*   Deleting documents<br><br>*   switch branch                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

<br/>

<br/>

<br/>

<br/>

*   **Software Test Design**

*   **Doc life cycle**
1.  Create Blank doc - create hub modal, from the repo page&homepage

2.  Create Draft - local draft marking, commit button milestone 1 Functionality

3.  Commit the doc - UI (color, Sizes), shows the changes that have been made, commit button is enable

4.  Discard draft

5.  Committed doc - View mode (UI adjustments, functionality)

6.  Committed doc - Edit mode (UI adjustments, functionality)

7.  Load an existing doc or draft

8.  Repo page drafts - marking, open the drafts
*   **Doc page**

*   ID & URL
1.  New Doc ID - URL

2.  Commit Doc ID - URL

3.  Draft Doc ID - ensure that draft ID does not exist, Generate new draft ID and save an empty draft

4.  Navigate Commit Doc - edit mode ID (URL)

5.  Navigate Commit Doc - view mode ID (URL)
*   **Load**
1.  exist draft - load draft (check `docId`)

2.  commit doc - load file (check `docId`)
*   **Commit action**
1.  Commit hub modal

2.  Commit draft

3.  Batch Commit

4.  Error message - commit (Titles, outdated)

5.  Commit X changes - the number change accordingly

6.  Commit button - X changes (the number change accordingly)
*   **Edge case**
1.  Draft on changes: create draft, make changes - load the draft & save the draft

2.  Batch commit - A combination between valid documents and those that cannot be committed (error message, commit button disable)
*   **Strass Test:**
1.  Batch commit 5 drafts

2.  Batch commit 5 drafts without title/content 

3.  Batch commit 5 drafts with reference to uncommitted docs 

4.  Discard draft in other draft

    <br/>
*   **Sanity test**
1.  Dummy Repo sanity test - doc page, load, commit action, batch commit

    <br/>
<br/>

1.  New Users
*   Connect as a new user 

*   Connect to to new workspace/connect to exist workspace 

*   Authorize git: 

    *   Authorize buttons 

    *   Authorize performance (check time)
<br/>

1.  Add repo
*   Add new repo 

    <br/>
2.  General Repo Page tests
*   Create docs, playlists

*   Add snippets, tokens, path to the doc/playlist

*   Commit the doc

*   Create Draft 

*   Doc to PR 

    <br/>
1.  Sidebar
*   Add repos 

*   Open repo

*   Switch between repos 

*   Open docs 

*   Switch workspace 

*   Add users

*   Doc life cycle

*   Doc page - ID & URL

*   Doc page - Load

*   Commit action

*   Edge case

    <br/>
<br/>

<br/>

<br/>

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/drownem5).
