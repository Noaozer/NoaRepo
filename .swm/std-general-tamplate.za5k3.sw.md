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

<br/>

<br/>

<br/>

ticket #864e8dv54 - Onboarding improvements

*   change the intro screen

*   change UI placement for the interactive screens

*   change set up account page's blurred background

*   if users skip onboarding, add a new card to the homepage that triggers the videos again.

STD -

<br/>

|**Test Case Type**          |**Description**                                                                  |**Test step**                                                                                                                                |**Expected Result**                                                                                                                                                                                                                          |**Status** (Pass/Fail)|
|----------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
|Functionally + compatibility|Intro screen                                                                     |1.  compare UI to figma<br><br>2.  Open the login screen in wide screen and narrow screen<br><br>3.  click start tour button<br><br>    <br/>|1.  UI look as figma<br><br>2.  Make sure that the intro screen adjusts itself to a standard screen size (24+ inches) and a laptop screen (14-16 inches)<br><br>3.  starts the tour and transfers to the interactive screens<br><br>    <br/>|<br/>                 |
|Functionally                |Interactive screens                                                              |1.  play every video in the interactive screens<br><br>2.  Click next and back<br><br>    <br/>                                              |1.  the video will be<br><br>2.  make sure you can skip between the interactive screens                                                                                                                                                      |<br/>                 |
|Functionally                |Skip - interactive screens                                                       |1.  click Skip in every interactive screen<br><br>2.  set up your account<br><br>    <br/>                                                   |1.  transfers to set up account page's blurred background<br><br>2.  a new card will be added to the homepage that triggers the videos again                                                                                                 |<br/>                 |
|Functionally                |Skip - Intro screen                                                              |1.  click Skip in intro screen<br><br>2.  set up your account                                                                                |1.  transfers to set up account page's blurred background<br><br>2.  a new card will be added to the homepage that triggers the videos again                                                                                                 |<br/>                 |
|Functionally                |On boarding tour through homepage<br><br>Homepage start with a quick product tour|1.  Skip on boarding start tour<br><br>2.  set up your account<br><br>3.  click - Start with a quick product tour<br><br>    <br/>           |1.  transfers to set up account page's blurred background<br><br>2.  UI look as figma - darkened background and the interactive screens will be in a different resolution<br><br>    <br/><br><br/>                                          |<br/>                 |

<br/>

|     |
|-----|
|<br/>|

<br/>

1.  on start dragging ➝ collapse the snippet if it was expanded

2.  on end drag ➝ bring the snippet to the state it was before the drag (expanded/collapsed)

3.  do not collapse out-of-sync/outdated snippets. - Why?

STD -

<br/>

|**Test Case Type**|**Description**                                             |**Test step**|**Expected Result**                                            |**Status (Pass/Fail)**|
|------------------|------------------------------------------------------------|-------------|---------------------------------------------------------------|----------------------|
|Functionally      |drag collapse snippet                                       |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |drag expanded snippet                                       |<br/>        |show the snippet being collapse                                |<br/>                 |
|<br/>             |drag expanded snippet + show more                           |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |\*\*\*drag new snippet with generative AI                   |<br/>        |make sure when draging it disappear end when droping its appear|<br/>                 |
|<br/>             |drop collapse snippet                                       |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |drop expanded snippet                                       |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |drop expanded snippet + show more                           |<br/>        |dont open show more when expanding                             |<br/>                 |
|<br/>             |drag&drop to the top part of the doc                        |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |drag&drop to the bottom of the doc                          |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |drag&drop between objects (table, mermaid, snippets, images)|<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |<br/>                                                       |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |<br/>                                                       |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |<br/>                                                       |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |<br/>                                                       |<br/>        |<br/>                                                          |<br/>                 |
|<br/>             |<br/>                                                       |<br/>        |<br/>                                                          |<br/>                 |

<br/>


<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 src/css/custom.css
```css
20     .docusaurus-highlight-code-line {
21       background-color: rgb(5666,129939393939, 91);
22       margin: 0 calc(-1 * var(--ifm-pre-padding));
23       padding: 0 var(--ifm-pre-padding);
24       /* its a try 
```

<br/>


<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 src/css/custom.css
```css
5       * work well for content-centric websites.
```

<br/>


<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
<!-- NOTE-swimm-repo ::dummy-repo:: -->
### 📄 examples/angular2/app/services/store.js
```javascript
1      var Todo = (function () {
2          function Todo(title) {
3              this.completed = false;
4              this.editing = false;
5              this.title = title.trim();
6          }
7          Object.defineProperty(Todo.prototype, "title", {
8              get: function () {
9                  return this._title;
10             },
11             set: function (value) {
12                 this._title = value.trim();
13             },
14             enumerable: true,
15             configurable: true
16         });
17         return Todo;
18     })();
```

<br/>

<br/>

<br/>

<br/>

<br/>


<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 package.json
<!-- collapsed -->

```json
2        "name": "docusaurus-template",
3        "version": "0.0.0",
4        "private": true,
5        "scripts": {
6          "docusaurus": "docusaurus",
7          "start": "docusaurus start",
8          "build": "docusaurus build",
9          "swizzle": "docusaurus swizzle",
10         "deploy": "docusaurus deploy",
11         "clear": "docusaurus clear",
12         "serve": "docusaurus serve",
13         "write-translations": "docusaurus write-translations",
14         "write-heading-ids": "docusaurus write-heading-ids"
15       },
```

<br/>

<br/>

<br/>

<br/>

<br/>

<br/>

<br/>

<br/>


<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
<!-- NOTE-swimm-repo ::dummy-repo:: -->
### 📄 examples/angular2/app/services/store.js
<!-- collapsed -->

```javascript
19     exports.Todo = Todo;
20     var TodoStore = (function () {
21         function TodoStore() {
22             var persistedTodos = JSON.parse(localStorage.getItem('angular2-todos') || '[]');
23             // Normalize back into classes
24             this.todos = persistedTodos.map(function (todo) {
25                 var ret = new Todo(todo._title);
26                 ret.completed = todo.completed;
```

<br/>


<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 src/css/custom.css
<!-- collapsed -->

```css
10       --ifm-color-primary: #25c2a0;
11       --ifm-color-primary-dark: rgb(33, 175, 144);
12       --ifm-color-primary-darker: rgb(31, 165, 136);
13       --ifm-color-primary-darkest: rgb(26, 136, 112);
14       --ifm-color-primary-light: rgb(70, 203, 174);
15       --ifm-color-primary-lighter: rgb(102, 212, 189);
```

<br/>

<br/>

<br/>

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBTm9hUmVwbyUzQSUzQU5vYW96ZXI=/docs/za5k3).
