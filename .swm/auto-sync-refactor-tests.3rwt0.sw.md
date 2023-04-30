---
id: 3rwt0
title: "Auto Sync Refactor Tests "
file_version: 1.1.2
app_version: 1.7.0
---

STP auto sync refactor

### Snippets

Functional tests:

*   change verify snippets to auto syncable - **in what terms?** (List all the cases) when it's verify the doc?

*   Accept auto syncable snippets - valid snippet, UI changes (Up to date, 2 green V, the right snippet display, Review Auto-Sync is empt - file is up to date)

*   Reselect atuo sync snippets

*   change snippets to outdated snippets - **in what terms?** (List all the cases) when it's verify the doc?

*   Reselect outdated snippets - valid snippet, UI changes (Up to date, 2 green V, the right snippet display, Review Auto-Sync is empt - file is up to date)

*   Remove outdated snippet

Draft test:

*   auto sync snippets in draft

*   outdated snippets in draft

Committed docs tests:

*   commit doc with auto syncable/outdated snippets

*   auto sync snippets in committed doc - View mode

*   auto sync snippets in committed doc - Edit mode

Workspaces review test:

*   auto syncable snippets review outdated

Edge case:

*   Auto-Syncable different sizes of snippets

*   Outdated different sizes of snippets

*   same snippets in the doc - make them auto sync/outdated

*   same snippets in different doc - make them auto sync/outdated

*   auto-syncable/outdated snippets with auto-syncable/outdated/verify token in the describe snippet

*   auto-syncable/outdated snippets with auto-syncable/outdated/verify token that appear in the snippets and in the describe snippet

*   change the code couple of times and make sure the last version is suggest in the auto-syncable snippets

*   change the code couple of times at the start to auto syncable and then to outdated and make sure the last version is suggest in the outdated snippet

Performance tests:

*   measure time to verify a doc with snippets

*   measure time to accept/reselect auto syncable snippets

*   measure time to remove/reselect outdated snippets
<br/>

### Tokens

Functional tests:

*   change verify tokens to auto syncable - **in what terms?** (List all the cases) when it's verify the doc?

*   Accept auto syncable tokens - valid token, UI changes (Token Up to date, 2 green V, the right token display, clicking on the token the right line appear, Review Auto-Sync is empty - file is up to date)

*   Reselect atuo sync token

*   change token to outdated tokens - **in what terms?** (List all the cases) when it's verify the doc?

*   Reselect outdated tokens - valid token, UI changes (Token Up to date, 2 green V, the right token display, clicking on the token the right line appear, Review Auto-Sync is empty - file is up to date)

*   Remove outdated token

*   add token to mermaid - auto syncable/outdated

Draft test:

*   auto sync tokens in draft

*   outdated tokens in draft

Committed docs tests:

*   commit doc with auto syncable/outdated tokens

*   auto sync tokens in committed doc - View mode

*   auto sync tokens in committed doc - Edit mode

Workspaces review test:

*   auto syncable tokens review outdated

Edge case:

*   same tokens in the doc - make them auto sync/outdated

*   same tokens in different doc at the workspaces - make them auto sync/outdated

*   auto-syncable/outdated snippets with auto-syncable/outdated/verify token in the describe snippet

*   auto-syncable/outdated snippets with auto-syncable/outdated/verify token that appear in the snippets and in the describe snippet

*   change the code couple of times and make sure the last version is suggest in the auto-syncable token

*   change the code couple of times at the start to auto syncable and then to outdated and make sure the last version is suggest in the outdated token
<br/>

Performance tests:

*   measure time to verify a doc with tokens

*   measure time to accept/reselect auto syncable tokens

*   measure time to remove/reselect outdated tokens
<br/>

### Paths

Functional tests:

`📄 docs`

*   change verify folder/file paths to auto syncable - **in what terms?** (List all the cases) when it's verify the doc?

*   Accept auto syncable folder/file paths - valid path, UI changes (path Up to date, 2 green V, the right path display, clicking on the path the folders/files open, Review Auto-Sync is empty - file is up to date)

*   Reselect atuo sync paths

*   change path to outdated path - **in what terms?** (List all the cases) when it's verify the doc?

*   Reselect outdated folder/file paths - valid path, UI changes (path Up to date, 2 green V, the right path display, clicking on the path the folders/files open, Review Auto-Sync is empty - file is up to date)

*   Remove outdated paths

Draft test:

*   auto sync paths in draft

*   outdated paths in draft

Committed docs tests:

*   commit doc with auto syncable/outdated paths

*   auto sync paths in committed doc - View mode

*   auto sync paths in committed doc - Edit mode

Workspaces review test:

*   auto syncable paths review outdated

Edge case:

*   same paths in the doc - make them auto sync/outdated

*   same paths in different doc at the workspaces - make them auto sync/outdated

*   auto-syncable/outdated paths with auto-syncable/outdated/verify paths in the describe snippet

*   change the folders couple of times and make sure the last version is suggest in the auto-syncable path

*   change the folders couple of times at the start to auto syncable and then to outdated and make sure the last version is suggest in the outdated path

Performance tests:

*   measure time to verify a doc with paths

*   measure time to accept/reselect auto syncable paths

*   measure time to remove/reselect outdated paths

### Integration

*   file with auto syncable snippets, tokens, paths

*   file with outdated snippets, tokens, paths

*   Review Auto Sync - right side bar
<br/>

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/3rwt0).
