---
id: 4xwjb
title: SWmd QA test
file_version: 1.1.2
app_version: 1.6.0
---

Test Plan:

# section 1 - write&read SWmd

1.  create a doc with editor commands **Markdown Syntax** all syntax from the table

2.  commit the doc

3.  go through SWmd:
*   compare the SWmd to the doc - make sure every syntax in SWmd represents command in the doc

*   male sure the file is written in mark down syntax

*   open the file - make sure Swimm read the file and shows every command right
1.  create a doc with that included not part of the markdown but part of the parser and serializer-
1.  Gapcursor (It's default but we need to make sure it works properly and not forgotten).

2.  History (doc history)

3.  Slash commands (WIP [https://tiptap.dev/experiments/commands](https://tiptap.dev/experiments/commands), we can base ourselves on it instead)

4.  Floating menu (TODO) - bubble menu

5.  Bubble menu (TODO) (AKA Context actions in the current editor)

6.  Keyboard shortcuts popover? (TODO) (Swimm shortcuts)

7.  Custom Paste (Markdown, Plaintext)

8.  Focus (Adds a class to the focused element for custom styling or logic)

9.  prosemirror-codemark (Third party) -Code block view

10.  AI stuff
2.  commit the doc

3.  go through SWmd:
*   compare the SWmd to the doc - make sure every syntax in SWmd represents command in the doc

*   male sure the file is written in mark down syntax

*   open the file - make sure Swimm read the file and shows every command right

    <br/>
1.  create a doc with editor commands **Swimm Syntax**\-
1.  (Code) Snippet

2.  (Smart) Token

3.  Doc/Playlist links (AKA Swimm links, just links to another doc).

4.  Mention

5.  Text/Snippet Template

6.  commit the doc

7.  go through SWmd:
*   compare the SWmd to the doc - make sure every syntax in SWmd represents command in the doc

*   make sure the file is written in Swimm new syntax
2.  open the file - make sure Swimm read the file and shows every command right
1.  create a doc with editor commands (Swimm + mark down syntax)

2.  try to break the syntax

3.  commit changes

4.  make sure the doc present all the commands (without break)

5.  go through SWmd:
*   compare the SWmd to the doc - make sure every syntax in SWmd represents command in the doc

    <br/>

# Section 2 - SWMD bugs

test cases:

1) code block - write `html + software language`

2) Use isDirectory in path symbol - We cannot rely on that field to exist in case we need that information in other places.

*   After fixing (2) - we should change `tokenizeSymbols` so it can take into consideration if a path is of type directory (using "isDirectory" field) - instead of letting it fail in case of trying to read folder contents.

3)RST docs import automatically - RST is a file format for textual data used primarily in the Python programming language community for technical documentation

3) Performance - While editing documents with a size-able amount of content there is an extremely noticeable amount of lag.

4) Images - using standard markdown the image didn’t display

5) provide common guidelines to convert .rst to .md

6) spaces, tabs, new lines do not persist

7) make a link italic - open the doc and you'll **not** see that it shows with `em` prefix

8) Editor - new line is added when saving a document between a bullet item and the line after it (reproduce it and check the SWmd)

9) SWMD on PRs - the line numbers changed and thus they see it as changes and it's a noise - use case swmd on PRs

10) Link Reuse in MD should be supported

11) Check use a standard MD Linter - and we should verify that our schema is adheres to it (Linter is a system that go through mark down syntax and make sure it's fine)

12) Austosync not working when using "collapse snippet"

**13) remove blobShas - cross repo names not removed ?**

14) picked the token `o` from this line of code - token is not parsed properly out of SWMD

15) Characters that break Smart Tokens -

*   backtick and then ' breaks a smart token

*   slashes breaks smart tokens

*   double quotes breaks after save and shown as outdated

*   A token followed by `)` - the parenthesis is hidden

*   `|` (table?) in the context breaks the token breaks

*   token with brackets breaks on draft

*   Typescript tokens with the type declarations adds a \`;' without the user writing it

*   Tokens: starting with / doesn't allow you to select the rest of the string

*   smart token starting with ^ rendered badly

*   smart tokens are saved with -1 wordIndexes - bug with global tokens that mis-parses words that have, for instance, a point inside of them. These tokens receive a -1 in their wordIndex - which is a bug.

*   smart tokens containing \[ and \` are not parsed properly

*   additional backticks are being added before smarttokens

16) Remove context from snippets on doc save - Now we create snippets without context, show them without the context (if it existed), but we never delete the context lines of existing snippets.

We should delete them, but it has **no real effect** right now except that people will still see the context lines when viewing/editing the doc raw.

17) Simple text with escapable characters - escape not removed on load

18) Encode SWMD title as '# Title' so that you can properly see the title in GitHub and other Markdown viewers

**19) The markdown generated by Swimm does not seem to render properly on Github ? - it should render also to git hub?**

*   Didn't know about the "rich view" in GitHub. This keeps coming back - they don't know they can use Swimm in an easier way **same**

20) Import from other tools - support folders

**21) It's hard for people to solve conflicts in** [**sw.md**](http://sw.md) **? Handle "real" merge conflicts in** [**sw.md**](http://sw.md) **(conflicts to the file blobs)?**

**22) Doc cannot be opened in the web due to extra spacings in the file\_blobs field - Someone from Orca accidentally ran Prettier or linter on this swmd file and it moved the file\_blobs one tab ahead which made the swmd parser to not being able to open it (no errors were shown, no logs). After reverting this change the doc can be loaded well - what is file blob?**

23) It wasn't clear that [sw.md](http://sw.md) files contain a link to the webapp

24)Importing a markdown file ➝ the content is blank

**25) Migrate from .swm to .**[**sw.md**](http://sw.md) **| Banner is missing padding - what the diff between them both?**

26) when there are 2 symbols on the same line in the swmd, smartext overrides the result of the first symbol with the one before

*   tokens that are on the same line in the same file override their applicability result

27) text rows should be shorter - split long rows - have a newline after 80 characters

28) Can't link in a pre-formatted code span - example: reate a pre-formatted code span using back ticks that is not a smart text. Try to add a link inside it.

29) View Doc Diff | Enhance CR experience when reviewing non-code changes in Swimm doc

30) Playlist External File(MD) | When viewing remote MD file that contains relative image - fails to view

31) swmd review experience: smart token ids change when the tokens don't - and it's weird to review (see image)

# Section 3 - regression bugs

# Section 4 - Document Title & Heading Levels

# Section 5 - Snippet file name header

# Section 6 - collapsed (snippet, anywhere else?)

# Section 7 - Playlist

# Section 8 - Front-Matter/Preamble (don't know)

# Section 9 - Link Text & Image Alt Text & Title (read about it, they can be a problem? included anchor headings and snippets?)

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/4xwjb).
