---
id: 4xwjb
title: SWmd QA test
file_version: 1.1.2
app_version: 1.7.0
---

Test Plan:

# Milestone 1

*   Create a new swmd (`@swimm/swmd`) package.

*   Bring in the bare minimum of parsing/serialization, editor component an so on.

*   Bring in the standalone demo app for developing the editor.

    *   Decide on what it should include. Do we want some debug panel in the main app?

*   TipTap Vue Devtools plugin?

*   Infrastructure for testing.

    *   vitest

    *   Cypress/Playwright component testing?

*   Integrate the new `SwmdEditor` component into the web app as a new page (Without most of the existing functionality of `EditDoc`), under a feature flag in the `.env` that will modify the router.

    *   TODO We might want something that can work at runtime?

*   Handle the interface between `SwmdEditor` and where to parse/serialize the doc, avoiding `v-model` cycles, and so on. (In particular the title component is outside the `SwmdEditor`.)

test -

# Milestone 2

*   New Drafts Store for the new format.

*   Save/Load (Commit) for the doc.

### Doc page - `https://app.swimm.io/workspaces/:workspaceId/repos/:repoId/branch/:branch/docs/:docId[/edit]`

**New**

*   Generate new draft ID and save an empty draft

*   Navigate to edit doc page

**Load**

*   if draft exists for `docId`:

    *   load draft

*   else:

    *   load file (Committed doc) (How? What code should I use for this?)

**On change**

*   Save the draft (Who? Debounce? Inidication of saving?)

**(Batch) Commit**

*   Commit the drafts

*   Save to database (How? What code should I use for this?)

test -

<br/>

<br/>

# section 1 - write&read SWmd

1.  create a doc with editor commands **Markdown Syntax** all syntax from the table

2.  commit the doc

3.  go through SWmd:
*   compare the SWmd to the doc - make sure every syntax in SWmd represents command in the doc

*   male sure the file is written in mark down syntax

*   open the file - make sure Swimm read the file and shows every command right
1.  create a doc with that included not part of the markdown but part of the parser and serializer-

2.  Gapcursor (It's default but we need to make sure it works properly and not forgotten).

3.  History (doc history)

4.  Slash commands (WIP [https://tiptap.dev/experiments/commands](https://tiptap.dev/experiments/commands), we can base ourselves on it instead)

5.  Floating menu (TODO) - bubble menu

6.  Bubble menu (TODO) (AKA Context actions in the current editor)

7.  Keyboard shortcuts popover? (TODO) (Swimm shortcuts)

8.  Custom Paste (Markdown, Plaintext)

9.  Focus (Adds a class to the focused element for custom styling or logic)

10.  prosemirror-codemark (Third party) -Code block view

11.  AI stuff

12.  commit the doc

13.  go through SWmd:
*   compare the SWmd to the doc - make sure every syntax in SWmd represents command in the doc

*   male sure the file is written in mark down syntax

*   open the file - make sure Swimm read the file and shows every command right

    <br/>
1.  create a doc with editor commands **Swimm Syntax**\-

2.  (Code) Snippet

3.  (Smart) Token

4.  Doc/Playlist links (AKA Swimm links, just links to another doc).

5.  Mention

6.  Text/Snippet Template

7.  commit the doc

8.  go through SWmd:
*   compare the SWmd to the doc - make sure every syntax in SWmd represents command in the doc

*   make sure the file is written in Swimm new syntax (view all symbols)
2.  open the file - make sure Swimm read the file and shows every command right

3.  create a doc with editor commands (Swimm + mark down syntax)

4.  try to break the syntax

5.  commit changes

6.  make sure the doc present all the commands (without break)

7.  go through SWmd:
*   compare the SWmd to the doc - make sure every syntax in SWmd represents command in the doc

    <br/>

# Section 2 - SWMD bugs

test cases:

according to category

1.  Adding code block - write in `html + software other language`

2.  Using isDirectory in path symbol - We cannot rely on that field to exist in case we need that information in other places. still using this field? do we replace it?

3.  symbol next to each other - without gap (see that nothing breaks and still looks the same)

4.  2 symbols on the same line in the swmd, smartext overrides the result of the first symbol with the one before

5.  tokens that are on the same line in the same file override their applicability result

6.  Import docs - RST docs import automatically (RST - is a file format for textual data used primarily in the Python programming language community for technical documentation)

7.  Importing a markdown file (the content is blank)

8.  Performance - While editing documents with a size-able amount of content there is an extremely noticeable amount of lag.

9.  Image symbol in swmd - using standard markdown the image (didn’t display in the previews swmd)

10.  Spaces - check spaces-tabs, new lines do not persist

11.  make a link italic - open the doc and you'll see that it shows with `em` prefix, make sure it doesn't happen

12.  Editor - new line is added when saving a document between a bullet item and the line after it (reproduce it and check the SWmd)

13.  use case SWMD on PRs - the line numbers changed and thus they see it as changes and it's a noise

14.  Using a standard MD Linter - verify that our schema is adheres to it (Linter is a system that go through mark down syntax and make sure it's fine)

15.  Auto sync when using 'collapse snippet' (not working)

16.  picked the token `o` from this line of code - token is not parsed properly out of SWMD

17.  check all Characters that break Smart Tokens -

18.  backtick and then ' breaks a smart token

19.  slashes breaks smart tokens

20.  double quotes breaks after save and shown as outdated

21.  A token followed by `)` - the parenthesis is hidden

22.  If you have smart token from line with | , the smart token is corrupted inside table

23.  link to doc inside table is broken if doc name contains | - have a doc whose name has | and add link to it inside table

24.  using || inside table creates extra columns - view after commit

25.  token with brackets breaks on draft

26.  Typescript tokens with the type declarations adds a \`;' without the user writing it

27.  Tokens: starting with / doesn't allow you to select the rest of the string

28.  smart token starting with ^ rendered badly

29.  smart tokens are saved with -1 wordIndexes - bug with global tokens that mis-parses words that have, for instance, a point inside of them. These tokens receive a -1 in their wordIndex - which is a bug

30.  text rows should be shorter - split long rows - have a newline after 80 characters

31.  View Doc Diff | Enhance CR experience when reviewing non-code changes in Swimm doc

32.  Playlist External File (MD) | When viewing remote MD file that contains relative image - fails to view

33.  swmd review experience: smart token ids change when the tokens don't - and it's weird to review

34.  Mermaid format - test changes in mermaid: replace the content and add context (new line, remove line, change line) , add token, change the template (Seems like now a change replacing new lines with<br/>
    is applied to the mermaid preview string, This means that after save the mermaid preview no longer works on github - the syntax is broken due to the added<br/>
    tags)

35.  A `<br/>` in a mermaid diagram breaks the diagram on save load - test this specific case and try to use the new syntex in the content mermaid to make sure it doesn't brake it either.

36.  **Didn't understand:**

37.  Link Reuse in MD should be supported **?**

38.  remove blobShas - cross repo names not removed **?**

39.  Doc cannot be opened in the web due to extra spacings in the file\_blobs field - Someone from Orca accidentally ran Prettier or linter on this swmd file and it moved the file\_blobs one tab ahead which made the swmd parser to not being able to open it (no errors were shown, no logs). After reverting this change the doc can be loaded well - what is file blob **?**

40.  "Github Enterprise Limitations" **what it means?**

    <br/>

# Document Title & Heading Levels

# Snippet file name header

# collapsed (snippet, anywhere else?)

# Playlist

# Front-Matter/Preamble (don't know)

# Link Text & Image Alt Text & Title (read about it, they can be a problem? included anchor headings and snippets?)

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/4xwjb).
