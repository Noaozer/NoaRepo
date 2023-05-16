---
id: 11cpd
title: stp + std sprint 9
file_version: 1.1.2
app_version: 1.8.0
---

### **Ticket - Review Auto-sync improvements**

Section - group order by logic for review auto-sync :

1.  Items in the "Review auto-sync" panel grouped by **resolution type**: "Autosyncable" and "Out of date" (UI as figma- icons, text...)

2.  Order in **"Auto syncable"** - by objects (token, snippets, path....) if the object has other mention in the doc they will be nested according to their location in the doc.

3.  Order in **"Outdated"** - by objects (token, snippets, path....) if the object has other mention in the doc they will be nested according to their location in the doc.

4.  **Clickable items** - Each item in the panel is clickable. clicking on an item will **scroll** and focus the document on the corresponding outdated code reference

5.  **The heading in nested item -** is leading to the first instance that - which is located first in the doc

6.  **Clickable items nested -** Each item in both "Autosyncable" and "Out of date" sections can represent a group of multiple instances

section - CTA - to accept or remove review items + animation - edit mode

1.  **Resolve Auto sync** - Accept all resolves all items at once **in a single transaction**

    *   allowing for a single undo action.

    *   No scrolling will occur in this case.

    *   When all the section's items are resolved - don't show the section.

2.  **Resolve Auto sync** - Accept each one (+nested) - click on the CTA button to resolve the item directly from the side bar (without going to its referenced place in the document) after clicking: The document will scroll to the referenced symbol, Animation, A micro animation will be shown in the doc itself (pre condition- edit mode)

3.  **Resolve Outdated** - Delete each one (+nested)

4.  **Resolve Outdated** - Replace each one (+nested

section - CTA - to accept or remove review items + animation - view mode

1.  Edit mode - no CTAs will be displayed, a message will be shown instead:

    "**Enter Edit mode** to resolve." The text "Enter Edit mode" will be a clickable button that switches to Edit mode when clicked.
<br/>

Section - notice section above :

1.  **text change** - "X code references were changed and this doc is now outdated.

    Resolve and commit them to keep this doc up to date." (UI as figma)

2.  **X count up according to the resolution** - add token, path, snippet, change/delete them, make sure

3.  **X count down changes according to resolution** - resolve auto sync + outdated object, make sure that the number is change

4.  **Show celebration animation on the sidebar when "resolve all"** - Animation: whole line fades to 0 opacity, then disappears

    STD table-

<br/>

|<br/>                          |<br/>                                                        |<br/>                                                                                                                                                                             |<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Test Case Type**             |**Description**                                              |**Pre-condition**                                                                                                                                                                 |**Test step**                                                                                                                                                                                                                                                                                                                                                                                                                                   |**Expected Result**                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|functionally/Usability/Security|Review Auto-Sync panel grouped by resolution type - view mode|\* document with auto-syncable/outdated items                                                                                                                                     |1\. open the doc - in view mode<br><br>2\. open the right side bar<br><br>3.  click on "Enter Edit mode"                                                                                                                                                                                                                                                                                                                                        |1\. Review Auto-Sync panel grouped by resolution type - Auto syncable section and Outdated section<br><br>2\. The auto-syncable and outdated items are grouped by resolution type in the review Auto-Sync panel<br><br>3\. No CTA's displayed next to the items<br><br>4\. there is a message: "Enter Edit mode to resolve."<br><br>5.  The text "Enter Edit mode" is clickable button that switches to Edit mode                                                                            |
|<br/>                          |Auto syncable and Outdated order                             |\* document with auto sync and outdated items<br><br>\* some of the items has instance                                                                                            |1\. open the doc - in a view mode<br><br>2\. open the right side bar                                                                                                                                                                                                                                                                                                                                                                            |1\. the review auto sync panel grouped by resolution type: "Autosyncable" and ""Out of date"<br><br>2\. the order in "Auto syncable" section is - by objects (token, snippets, path....) if the object has other mention in the doc they will be nested according to their location in the doc.<br><br>3\. the order in "Outdated" section is - by objects (token, snippets, path....) if the object has other mention in the doc they will be nested according to their location in the doc.|
|<br/>                          |UI - "Review auto-sync" panel                                |\* document with X auto syncable and outdated items                                                                                                                               |1\. open the document<br><br>2\. open the right side bar<br><br>3\. compare UI to Figma<br><br>4\. switch to edit mode<br><br>5\. compare UI to Figma                                                                                                                                                                                                                                                                                           |1\. the UI looks as Figma - in view mode _no CTA's_ notice section above - "Enter Edit mode to resolve."<br><br>2\. the UI looks as Figma - on view mode _there is CTA's_ notice section above - "X code references were changed and this doc is now outdated. Resolve and commit them to keep this doc up to date.""                                                                                                                                                                        |
|<br/>                          |Clickable items                                              |\* document with auto sync and outdated items                                                                                                                                     |1\. open the doc<br><br>2\. open the right side bar<br><br>3\. click on the items in the review auto sync panel<br><br>4\. switch to edit mode<br><br>5\. click on the items in the review auto sync panel                                                                                                                                                                                                                                      |1\. Each item in the panel is clickable in view mode and in edit mode.<br><br>2\. Clicking on an item will scroll and focus the document on the corresponding outdated code reference.                                                                                                                                                                                                                                                                                                       |
|<br/>                          |Clickable items - nested                                     |\* document with auto sync and outdated items - each item has multiple instances                                                                                                  |1\. open the doc<br><br>2\. open the right side bar<br><br>3\. click on each item in both "Auto syncable" and "Out of date"sections that represent a group of multiple instances (the heading<br><br>4\. click on every instance<br><br>5\. switch to edit mode<br><br>6\. click on each item in both "Auto syncable" and ""Out of date"" sections that represent a group of multiple instances (the heading)<br><br>7\. click on every instance|1\. clicking on the heading in nested item is leading (scroll and focus) to the first instance which is located first in the doc - in view and edit mode<br><br>2\. clicking on the the instances in nested item is leading (scroll and focus) to the instance in the doc - in view and edit mode                                                                                                                                                                                            |
|<br/>                          |CTA 's to accept or remove review items - edit mode          |\* document that has auto sync and outdated items<br><br>\* some of the item in both "Autosyncable"<br><br>and ""Out of date" sections can represent a group of multiple instances|1\. open the doc<br><br>2\. open the right side bar<br><br>3\. switch to edit mode<br><br>4\. compare UI to Figma                                                                                                                                                                                                                                                                                                                               |1\. Next to each item, there is a Call-To-Action (CTA) button (UI as Figma) to resolve the item directly from the sidebar without going to its referenced place in the document - the CTA's appears only in Edit mode                                                                                                                                                                                                                                                                        |
|<br/>                          |CTA - Auto syncable accept item                              |\* document with auto syncable items (tokens, snippets, path)                                                                                                                     |1\. open the doc<br><br>2\. open the right side bar<br><br>3\. switch to edit mode<br><br>4\. at the preview auto sync section - click on the V icon to accept(the item is from the auto syncable group)                                                                                                                                                                                                                                        |1\. The document will scroll to the referenced symbol<br><br>2\. Animation: the whole line fades to 0 opacity, then disappears<br><br>3\. A micro animation will be shown in the doc itself (According to the item)                                                                                                                                                                                                                                                                          |
|<br/>                          |CTA - Outdated remove item                                   |\* document with outdated items (tokens, snippets, path, doc)                                                                                                                     |1\. open the doc<br><br>2\. open the right side bar<br><br>3\. switch to edit mode<br><br>4\. at the preview auto sync in outdated section - click on the remove icons                                                                                                                                                                                                                                                                          |1\. The document will scroll to the referenced symbol<br><br>2\. Animation: the whole line fades to 0 opacity, then disappears<br><br>3\. A micro animation will be shown in the doc itself (According to the item)                                                                                                                                                                                                                                                                          |
|<br/>                          |Resolve Auto sync - Accept all                               |\* document with auto syncable items (tokens, snippets, path)<br><br>\* some item in both "Autosyncable"<br><br>section represent a group of multiple instances                   |1\. open doc on edit mode<br><br>2\. open right side bar<br><br>3\. click accept all on review auto syncable<br><br>4\. Undo (c+z)                                                                                                                                                                                                                                                                                                              |1\. Accept all resolves all items at once in a single transaction<br><br>2\. No scrolling will occur in this case<br><br>3\. When all the section's items are resolved - Auto syncable section doesn't appear<br><br>4\. undo to accept all action return all auto syncable items to the doc and to the preview auto syncable section                                                                                                                                                        |
|<br/>                          |Resolve all items                                            |\* document with auto syncable and outdated items                                                                                                                                 |1\. open the doc in edit mode<br><br>2\. open the right side bar<br><br>3\. accept all auto syncable items<br><br>4\. remove all outdated items                                                                                                                                                                                                                                                                                                 |1\. after accept all auto syncable items - the auto-syncable section does not appear<br><br>2\. after remove all outdated items - the Outdated section does not appear<br><br>3\. review Auto-sync section is empty<br><br>4\. celebration animation on the sidebar ""resolve all"" - Animation: whole line fades to 0 opacity, then disappears                                                                                                                                              |

<br/>

**Review Auto-sync improvements 10**

### **C50: Review Auto-Sync panel grouped by resolution type - view mode**

<br/>

|<br/>                  |<br/>           |<br/>           |<br/>             |
|-----------------------|----------------|----------------|------------------|
|**Type**Functional     |**Priority**High|**Estimate**None|**References**None|
|**Automation Type**None|<br/>           |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document with auto-syncable/outdated items
<br/>

#### Steps

1.  open the doc - in view mode

2.  open the right side bar

3.  click on "Enter Edit mode"

#### Expected Result

1.  Review Auto-Sync panel grouped by resolution type - Auto syncable section and Outdated section

2.  The auto-syncable and outdated items are grouped by resolution type in the review Auto-Sync panel

3.  No CTA's displayed next to the items

4.  there is a message: "Enter Edit mode to resolve."

5.  The text "Enter Edit mode" is clickable button that switches to Edit mode

### **C51: Auto syncable and Outdated order**

<br/>

|<br/>                  |<br/>           |<br/>           |<br/>             |
|-----------------------|----------------|----------------|------------------|
|**Type**Functional     |**Priority**High|**Estimate**None|**References**None|
|**Automation Type**None|<br/>           |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document with auto sync and outdated items

*   some of the items has instance

#### Steps

1.  open the doc - in a view mode

2.  open the right side bar

#### Expected Result

1.  the review auto sync panel grouped by resolution type: "Autosyncable" and "Out of date"

2.  the order in "Auto syncable" section is -  by objects (token, snippets, path....) if the object has other mention in the doc they will be nested according to their location in the doc.

3.  the order in "Outdated" section is - by objects (token, snippets, path....)  if the object has other mention in the doc they will be nested according to their location in the doc.

### **C52: UI - "Review auto-sync" panel**

<br/>

|<br/>                  |<br/>             |<br/>           |<br/>             |
|-----------------------|------------------|----------------|------------------|
|**Type**Compatibility  |**Priority**Medium|**Estimate**None|**References**None|
|**Automation Type**None|<br/>             |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document with X auto syncable and outdated items

#### Steps

1.  open the document

2.  open the right side bar

3.  compare UI to Figma

4.  switch to edit mode

5.  compare UI to Figma

#### Expected Result

1.  the UI looks as Figma - in view mode<br/>
    \*no CTA's<br/>
    \*notice section above - "Enter Edit mode to resolve."

2.  the UI looks as Figma - on view mode<br/>
    \*there is CTA's<br/>
    \*notice section above - "X code references were changed and this doc is now outdated.<br/>
    Resolve and commit them to keep this doc up to date."

### **C53: Clickable items**

<br/>

|<br/>                  |<br/>               |<br/>           |<br/>             |
|-----------------------|--------------------|----------------|------------------|
|**Type**Performance    |**Priority**Critical|**Estimate**None|**References**None|
|**Automation Type**None|<br/>               |<br/>           |<br/>             |

<br/>

#### Preconditions

\*document with auto sync and outdated items

#### Steps

1.  open the doc

2.  open the right side bar

3.  click on the items in the review auto sync panel

4.  switch to edit mode

5.  click on the items in the review auto sync panel

#### Expected Result

1.  Each item in the panel is clickable in view mode and in edit mode.

2.  Clicking on an item will scroll and focus the document on the corresponding outdated code reference.

### **C54: Clickable items - nested**

<br/>

|<br/>                  |<br/>               |<br/>           |<br/>             |
|-----------------------|--------------------|----------------|------------------|
|**Type**Functional     |**Priority**Critical|**Estimate**None|**References**None|
|**Automation Type**None|<br/>               |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document with auto sync and outdated items - each item has multiple instances

#### Steps

1.  open the doc

2.  open the right side bar

3.  click on each item in both "Autosyncable" and "Out of date" sections that represent a group of multiple instances (the heading)

4.  click on every instance

5.  switch to edit mode

6.  click on each item in both "Autosyncable" and "Out of date" sections that represent a group of multiple instances (the heading)

7.  click on every instance

#### Expected Result

1.  clicking on the heading in nested item is leading (scroll and focus) to the first instance which is located first in the doc - in view and edit mode

2.  clicking on the the instances in nested item is leading (scroll and focus) to the instance in the doc - in view and edit mode

### **C55: CTA 's to accept or remove review items - edit mode**

<br/>

|<br/>                  |<br/>               |<br/>           |<br/>             |
|-----------------------|--------------------|----------------|------------------|
|**Type**Compatibility  |**Priority**Critical|**Estimate**None|**References**None|
|**Automation Type**None|<br/>               |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document that has auto sync and outdated items

*   some of the item in both "Autosyncable" and "Out of date" sections can represent a group of multiple instances

#### Steps

1.  open the doc

2.  open the right side bar

3.  switch to edit mode

4.  compare UI to Figma

#### Expected Result

1.  Next to each item, there is a Call-To-Action (CTA) button (UI as Figma) to resolve the item directly from the sidebar without going to its referenced place in the document - the CTA's appears only in Edit mode

### **C56: CTA - Autosyncable accept item**

<br/>

|<br/>                  |<br/>             |<br/>           |<br/>             |
|-----------------------|------------------|----------------|------------------|
|**Type**Other          |**Priority**Medium|**Estimate**None|**References**None|
|**Automation Type**None|<br/>             |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document with auto syncable items (tokens, snippets, path)

#### Steps

1.  open the doc

2.  open the right side bar

3.  switch to edit mode

4.  at the preview auto sync section - click on the V icon to accept(the item is from the auto syncable group)

#### Expected Result

1.  The document will scroll to the referenced symbol

2.  Animation: the whole line fades to 0 opacity, then disappears

3.  A micro animation will be shown in the doc itself (According to the item)

### **C57: CTA - Outdated remove item**

<br/>

|<br/>                  |<br/>               |<br/>           |<br/>             |
|-----------------------|--------------------|----------------|------------------|
|**Type**Functional     |**Priority**Critical|**Estimate**None|**References**None|
|**Automation Type**None|<br/>               |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document with outdated items (tokens, snippets, path, doc)

#### Steps

1.  open the doc

2.  open the right side bar

3.  switch to edit mode

4.  at the preview auto sync in outdated section - click on the remove icons

#### Expected Result

1.  The document will scroll to the referenced symbol

2.  Animation: the whole line fades to 0 opacity, then disappears

3.  A micro animation will be shown in the doc itself (According to the item)

### **C58: Resolve Auto sync - Accept all**

<br/>

|<br/>                  |<br/>               |<br/>           |<br/>             |
|-----------------------|--------------------|----------------|------------------|
|**Type**Functional     |**Priority**Critical|**Estimate**None|**References**None|
|**Automation Type**None|<br/>               |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document with auto syncable items (tokens, snippets, path)

*   some item in both "Autosyncable" section represent a group of multiple instances

#### Steps

1.  open doc on edit mode

2.  open right side bar

3.  click accept all on review auto syncable

4.  Undo (c+z)

#### Expected Result

1.  Accept all resolves all items at once in a single transaction

2.  No scrolling will occur in this case

3.  When all the section's items are resolved - Auto syncable section doesn't appear

4.  undo to accept all action return all auto syncable items to the doc and to the preview auto syncable section

### **C59: Resolve all items**

<br/>

|<br/>                  |<br/>           |<br/>           |<br/>             |
|-----------------------|----------------|----------------|------------------|
|**Type**Functional     |**Priority**High|**Estimate**None|**References**None|
|**Automation Type**None|<br/>           |<br/>           |<br/>             |

<br/>

#### Preconditions

*   document with auto syncable and outdated items

#### Steps

1.  open the doc in edit mode

2.  open the right side bar

3.  accept all auto syncable items

4.  remove all outdated items

#### Expected Result

1.  after accept all auto syncable items - the auto-syncable section does not appear

2.  after remove all outdated items - the Outdated section does not appear

3.  review Auto-sync section is empty  

4.  celebration animation on the sidebar "resolve all" - Animation: whole line fades to 0 opacity, then disappears

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/11cpd).
