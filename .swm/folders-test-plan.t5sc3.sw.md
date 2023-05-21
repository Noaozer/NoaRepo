---
id: t5sc3
title: "Folders Test Plan "
file_version: 1.1.2
app_version: 1.9.0
---

**Intro**

Folders is a new feature that allows users to create folders which are shown in the repo page, In order to organize docs in Swimm.

The development of the folders feature involves behavior changes, UI/UX changes that should pass quality assurance tests.

**Preconditions**

*   Setting up a testing environment after development is complete

*   Comprehensive testing plan (STP,STD)

**Testing Environment**

*   Dev local/Staging

*   variable workspaces

**Testing strateg**

*   Performing QA tests in a continuous interface with the development team (Orbit) and fixing bugs on an ongoing basis

*   Receiving rejections from UX/PM and fixing them until the next version is released

*   Regression - 2nd QA round
1.  After QA testing session and the bug fixes an additional session will be conducted that will include regression testing in order to make sure that fixing a bug did not create a new bug

2.  The tests will be written later according to the results of the first round

    <br/>

**Software Test Plan**

*   Functional Tests

Creating Folders:

1.  New buttons functionality

2.  Keyboard functionality

3.  Validation tests on text fields (folders name)

4.  Create folders - repo page button, move to folder hub modal

5.  Create sub folder - + icon, move to folder hub modal

6.  Create icon - creating documents/playlists/subfolders through an existing folder

7.  Empty folder - state

8.  Create folder with docs only in main - State

9.  Create folder with docs only in branch - switch between branch (docs) and main (state)

10.  Create doc in a folder and commit it to a new branch and start a pr

11.  Create PR branch docs in folder - Check main state - \`this folder only contains docs/playlist - they will be listed here upon merge'

12.  Merge PR branch docs in folder - check main upon merge branch the docs listed in the same folder in main
<br/>

Folder Functionality:

1.  Folder ellipsis functionality - rename/delete/move to folder

2.  Pin playlists inside folders

3.  Documents in the folder are displayed correctly

4.  batch commit to all documents in the folder

5.  batch commit to some of the documents in the folder

6.  discard documents that are in the folder

7.  Drafts docs/playlists saves as part of the folder

8.  Combine drafts and committed docs/playlists as part of the folder

9.  In the same folder commit doc/playlist from different branches

10.  In the same folder saves drafts doc/playlist from different branches

11.  Combine drafts and committed docs/playlists as part of from different branches the same folder

12.  Reordering files and folders

Move to folder:

1.  Move to folder hub modle - functionality, Keyboard functionality

2.  create new folder

3.  Relocate documents/playlists/subfolders into a folder through ellipsis

4.  Relocate documents/playlists/subfolders outside the folder - check order in repo page

5.  Relocate documents/playlists/subfolders to different folder

6.  Drag&Drop functionality - drag&drop folders to move items, reordering items with Drag & drop, move docs/drafts/playlist in a folder

7.  Batch action - check box functionality (move)

8.  move to folder - ellipsis next to share (edit&view mode)

Display:

1.  light/dark theme

2.  View Swimm documents in hierarchical order at the repo page

3.  In this branch section - document display division (Changed in current branch and documents list)

4.  Folder view switch - and back to Repo

5.  Filter: Folders - folders

6.  Search subdolders/docs and playlists in a folder

7.  Search docs/playlist - Show doc path in search dialog

8.  Editor anatomy - hover, select a folder, move to folder hub model

9.  Change order using - Name, Status, Author, Last Modified

10.  Open folder - move between branches

11.  Create in current branch table - Routing to the folder where the document is located
<br/>

*   User Interface - Compatibility tests
1.  [Figma](https://www.figma.com/file/J0WvA8KssUSd1xJM933B1L/Folder-Hierarchy-%26-Doc-Sidebar?type=design&node-id=1576-126901&t=2JM0rLwBmLsCHDVy-0) - design compatibility

2.  Compatibility tests (icon sizes, locations, etc.)

    <br/>
*   User Experience - Usability tests
1.  Intuitive buttons

2.  Easy to use and understand

    <br/>
*   Destructive - Edge cases
1.  Error messages

2.  explaining why the confirm button is disabled

3.  Long folder name (overflow ellipsis)

4.  Several subfolders within a folder

5.  folders with the same name

6.  Move outdated documents and local draft into the folder

7.  Delete folder with docs/playlist/sub folders that are committed to different branche

8.  Delete folder with docs/playlist/sub folders that are committed to different branches

9.  Delete folder with docs/playlist/sub folders that are committed to different branches

10.  demo repo - without folders

11.  reordering docs in demo repo is disabled

12.  Drag folder into the same itself
<br/>

*   Sanity test
1.  Repo page - move between sections

2.  Doc flow

3.  Editor flow

    <br/>
*   Performance
1.  Measuring time for changing a branch - verify the distribution of changed documents and a list of documents

2.  Measuring time for batch commit to all documents in the folder

3.  Measuring time for moving a lot of documents/playlist/folder to a folder

4.  Measuring time for deleting a folder with lot of documents/playlist/folder
*   Regression:
1.  Canceling folder creation with esc (with or without a name)

2.  draft document created through a folder (+ icon) cannot be moved outside the folders

3.  Deleting a doc from ellipsis menu does not remove it from its folder

4.  drag folder into the same itself and then everything stuck

5.  Changed in current branch section | Going to a branch with a new playlist doesn't show the playlist in the "Changed in current branch" section
<br/>

*   Automated
1.  automated tests - E2E
<br/>

*   Security Test - Folders Analytics
1.  The events sent do not contain sensitive information

    <br/>
<br/>

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/t5sc3).
