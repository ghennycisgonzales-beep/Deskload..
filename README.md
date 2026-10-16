Deskload — Student Task Tracker & Weekly Workload Planner

Isang web-based na task manager para sa mga estudyante. Dito nila nilalagay ang assignments, readings, at exams, tapos makikita agad kung alin ang overdue, due today, at kung aling subject ang pinakamabigat.

Live demo: https://ghennycisgonzales-beep.github.io/Deskload/ Members: [mga pangalan] | Course: [course code] | Instructor: [pangalan] | BSIT, 2026

Ito ay front-end prototype (Week 1). Walang server at database pa. Ang data ay nasa browser lang gamit ang LocalStorage.

Mga Feature
Mag-add ng task na may title, due date, subject, at priority
I-mark bilang tapos (checkbox) o i-delete ang task (✕)
Awtomatikong Overdue at Due today na label
Dashboard statistics: Open, Due Today, Overdue, Completed
Workload by subject na bar chart (open tasks lang)
Tuloy-tuloy ang data kahit i-close ang browser
Tamang petsa ayon sa local time (Pilipinas) sa Overdue / Due today
Responsive (mobile-friendly) at may awtomatikong dark mode
Reset all data button para bumalik sa sample tasks
Paano ito gumagana

Ang mga bahagi ng system:

Component	Teknolohiya	Tungkulin
Interface	HTML5 + CSS3	Form, task table, dashboard, styling
Logic	JavaScript (ES6+)	Add, complete, delete, deadline check, render
Storage	LocalStorage (Web Storage API)	Pag-save ng tasks sa browser ng user
Format ng data	JSON	JSON.stringify() para i-save, JSON.parse() para basahin
Fonts	Google Fonts	Source Serif 4 (headings), IBM Plex Sans (text)
Mga function sa index.html
Function	Ginagawa
loadTasks()	Binabasa ang tasks mula LocalStorage; kung wala, tumatawag ng seedTasks()
seedTasks()	Gumagawa ng 3 sample tasks
addTask()	Kinukuha ang laman ng form, gumagawa ng task object, nagse-save, nagre-render
toggleDone(id)	Binabago ang status ng task (tapos / hindi pa)
deleteTask(id)	Tinatanggal ang task
saveTasks(tasks)	Kino-convert sa JSON at sine-save sa LocalStorage (may try...catch)
toLocalISO(date)	Ginagawang YYYY-MM-DD ang petsa gamit ang local time
dueClass() / dueLabel()	Kinukumpara ang due date sa petsa ngayon para sa Overdue / Due today
render()	Nag-a-update ng stats, task table, at workload bars
escapeHtml()	Pinipigilan na masira ang page kung may special characters ang input
resetAll()	Ibinabalik sa sample tasks
Task object
js
{ id, title, subject, due, priority, done }
Daloy ng sistema
LocalStorage
JavaScript
Deskload Interface
User
LocalStorage
JavaScript
Deskload Interface
User
Buksan ang page
loadTasks()
Basahin ang deskload_tasks_v1
Tasks (o wala, kaya seedTasks())
render()
Punan ang form, pindutin ang Add task
addTask()
saveTasks() (JSON)
render()
Check / ✕ sa task
toggleDone(id) / deleteTask(id)
saveTasks()
render()

Mga hakbang:

Pagbukas ng page, tinatawag ang loadTasks() para kunin ang naka-save na tasks.
Kapag walang naka-save, gumagawa ng 3 sample tasks.
Pag-add ng task, gumagawa ng object na may unique id.
Sine-save ang buong listahan bilang JSON sa LocalStorage (key: deskload_tasks_v1).
Tinatawag ang render(), na iisang function na nagre-refresh ng buong screen.
Sa bawat render, kinukumpara ang due date sa petsa ngayon at kinukwenta ang stats at workload.
Project structure
Deskload/
├── index.html   # Buong app (HTML + CSS + JavaScript)
└── README.md    # Dokumentasyong ito
Paano i-run

Online: buksan ang live demo link sa taas.

Local:

bash
git clone https://github.com/ghennycisgonzales-beep/Deskload.git
cd Deskload
#  index.html

Walang kailangang i-install, walang server.

LocalStorage
Key	Laman
deskload_tasks_v1	Listahan ng lahat ng tasks (JSON)
Troubleshooting
Problema	Solusyon
Nawala ang mga tasks	Hiwalay ang LocalStorage kada browser, kada link, at kapag naka-incognito. I-check kung pareho ang browser at link na ginamit
Sample tasks lang ang lumalabas	Wala pang naka-save sa browser na ito, o na-click ang Reset all data
404 sa GitHub Pages	Siguraduhing index.html ang pangalan ng file at naka-set ang Pages sa main / root
Iba ang font	Kailangan ng internet ang Google Fonts; gagana pa rin ang app kahit wala
Hindi nagse-save ang task	Posibleng naka-block ang LocalStorage (private mode); hindi magka-crash ang app dahil sa try...catch
Mga limitasyon
Ang data ay nasa isang browser lang; walang accounts at walang sync sa ibang device
Walang edit feature para sa existing task (delete at add ulit)
Ang priority ay ipinapakita lang; hindi ito ginagamit sa pag-sort
Front-end prototype pa lang ito
Mga posibleng pagpapabuti
Gumawa ng TaskService REST API (create, complete, list) sa backend
Database at user accounts para sa online storage at multi-device access
Edit feature at sorting ayon sa priority
PWA (manifest at service worker) para ma-install at gumana offline
Tech stack

HTML5 · CSS3 · JavaScript (ES6+) · LocalStorage · Google Fonts

References (MDN Web Docs)
HTML: https://developer.mozilla.org/en-US/docs/Web/HTML
CSS: https://developer.mozilla.org/en-US/docs/Web/CSS
JavaScript: https://developer.mozilla.org/en-US/docs/Web/JavaScript
CSS custom properties: https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties
prefers-color-scheme: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme
Flexbox: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexbox
CSS Grid: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout
Media queries: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries
Web Storage API: https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API
JSON: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON
Array methods: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array
Template literals: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals
Date: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date
DOM: https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model
try...catch: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch

1. Core Web Languages
These three technologies form the foundation of the Deskload web interface.
1.1 HTML5 — Website Structure
HTML stands for HyperText Markup Language. It defines the structure and content of a webpage.
In Deskload, HTML can provide:
- The application heading and labels
- Input fields for task details
- Buttons for adding or managing tasks
- Tables or lists for displaying assignments
Example:
<h1>Deskload</h1>
<input type="text" placeholder="Task name">
<button>Add Task</button>
Simple explanation: HTML is like the framework of a house. It defines the parts that exist on the page.
Official documentation: MDN — HTML
1.2 CSS3 — Design and Appearance
CSS stands for Cascading Style Sheets. It controls colors, fonts, spacing, alignment, and page layout.
In Deskload, CSS can be used to:
- Set the page and header colors
- Style buttons and input fields
- Space out forms and task lists
- Make the layout adapt to different screen sizes
Example:
body {
  background: #f5f2eb;
  color: #202a35;
  font-family: sans-serif;
}
Simple explanation: If HTML is the framework of a house, CSS is its paint, decoration, and arrangement.
Official documentation: MDN — CSS
1.3 JavaScript (ES6+) — Application Functionality
JavaScript adds behavior and interactivity to a webpage. ES6+ refers to modern JavaScript features introduced in ECMAScript 2015 and later versions.
In Deskload, JavaScript can handle:
- Adding, editing, and deleting tasks
- Marking tasks as complete
- Calculating overdue and due-today counts
- Filtering or sorting assignments
- Saving task data in the browser
Example:
const taskName = "Multimedia assignment";
console.log(taskName);
Simple explanation: HTML creates the structure, CSS controls the appearance, and JavaScript makes the application respond to user actions.
Official documentation: MDN — JavaScript
2. CSS Techniques
2.1 CSS Custom Properties (Variables)
CSS custom properties store reusable values, such as colors, under names beginning with --.
Example:
:root {
  --navy: #172b40;
  --paper: #f5f2eb;
  --ink: #202a35;
}

body {
  background: var(--paper);
  color: var(--ink);
}

header {
  background: var(--navy);
}
- --navy, --paper, and --ink are custom properties.
- var(--paper) uses the value stored in --paper.
- Changing a variable can update every element that uses it.
Why it is useful: It keeps the color theme consistent and makes design changes easier.
Documentation: MDN — Using CSS custom properties
2.2 prefers-color-scheme — Light and Dark Mode Preference
This media feature detects whether the user's operating system or browser indicates a preference for a light or dark color scheme.
Example:
body {
  background: white;
  color: black;
}

@media (prefers-color-scheme: dark) {
  body {
    background: #172b40;
    color: white;
  }
}
When the preference is dark, the second rule applies. A website needs suitable CSS rules for dark mode; the media query does not redesign the whole page automatically.
Why it is useful: It can make Deskload more comfortable for users who prefer dark interfaces.
Documentation: MDN — prefers-color-scheme
2.3 Flexbox — One-Dimensional Layout
Flexbox arranges elements in a row or column.
Example:
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
}
- display: flex creates a flex container.
- justify-content controls alignment along the main axis.
- align-items controls alignment along the cross axis.
- gap adds space between items.
Deskload example: Flexbox can place the application title on one side and statistics or action buttons on the other.
Documentation: MDN — CSS Flexible Box Layout
2.4 CSS Grid — Rows and Columns
CSS Grid arranges content in two dimensions: rows and columns.
Example:
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
}
This creates two equal-width columns. 1fr represents one fraction of the available space.
Deskload example: One column can contain the task form, while another displays the task list.
Flexbox vs. Grid: Flexbox is generally best for a one-dimensional row or column. Grid is designed for two-dimensional layouts.
Documentation: MDN — CSS Grid Layout
2.5 Responsive Design and Media Queries
Responsive design helps a webpage adapt to different screen sizes. A media query applies CSS only when a condition is met.
Example:
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

@media (max-width: 860px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
- Above 860 pixels, the layout has two columns.
- At 860 pixels or narrower, it switches to one column.
The 860px breakpoint is a design choice, not a universal web requirement.
Why it is useful: It makes the interface easier to use on phones, tablets, and desktop screens.
Documentation: MDN — Using media queries
2.6 Viewport Meta Tag
The viewport meta tag helps mobile browsers size the webpage to the device's viewport.
Example:
<meta name="viewport" content="width=device-width, initial-scale=1">
- width=device-width sets the viewport width to the device width.
- initial-scale=1 sets the initial zoom level.
Without it, a desktop-oriented webpage may appear too small on a phone.
Important: This tag helps with responsive design, but it does not by itself make a website an installable Progressive Web App (PWA).
Documentation: MDN — Viewport meta element
3. JavaScript and Web APIs
3.1 localStorage — Saving Data in the Browser
localStorage is a browser API that stores string data for a website origin. Data usually remains available after the browser is closed and reopened.
Example:
localStorage.setItem("studentName", "Student");
const name = localStorage.getItem("studentName");
In Deskload, it can store tasks so they can be loaded again during a later visit in the same browser and origin.
A typical workflow is:
1. The user adds a task.
2. JavaScript saves the task data in localStorage.
3. When the application loads again, JavaScript reads the saved data and displays the tasks.
Limitations:
- It is browser storage, not a centralized database.
- Data does not automatically sync across devices.
- Clearing browser data can remove saved tasks.
- Storage access or writes can fail, so error handling is important.
Documentation:
- MDN — Window.localStorage
- MDN — Web Storage API
3.2 JSON.stringify() and JSON.parse() — Converting Data
localStorage stores strings. Task objects therefore need to be converted into JSON text before saving and parsed when loading.
Example task object:
const task = {
  title: "Finish assignment",
  subject: "CIT 742",
  completed: false
};
JSON.stringify() converts supported JavaScript data into a JSON string:
const savedTask = JSON.stringify(task);
localStorage.setItem("task", savedTask);
JSON.parse() converts JSON text back into a JavaScript value:
const loadedTask = JSON.parse(
  localStorage.getItem("task")
);
Why it is useful: It allows Deskload to save and reload structured task information.
Documentation: MDN — JSON
3.3 Array Methods — .map(), .filter(), and .sort()
An array stores a collection of values or objects. Deskload can use an array to hold multiple tasks.
Example:
const tasks = [
  { title: "HTML activity", completed: false },
  { title: "Python exercise", completed: true },
  { title: "Java project", completed: false }
];
.map() — Transform each item
const titles = tasks.map(task => task.title);
Result:
["HTML activity", "Python exercise", "Java project"]
map() creates a new array from the results of calling a function on each item. It can be used to extract task titles or prepare data for display.
.filter() — Keep items that meet a condition
const unfinished = tasks.filter(
  task => !task.completed
);
The result contains only the HTML activity and Java project. filter() is useful for showing pending, completed, or overdue tasks.
.sort() — Order items
const numbers = [3, 1, 2];
numbers.sort((a, b) => a - b);
Result: [1, 2, 3].
In Deskload, a comparison function can sort tasks by due date. Note that sort() changes the original array; use a copy first if the original order must be preserved.
Documentation: MDN — Array
3.4 Template Literals — Building Dynamic Strings
Template literals use backticks and ${...} to insert values or expressions into strings.
Example:
const taskName = "Python exercise";
const message = `Your task is ${taskName}.`;
Result: Your task is Python exercise.
Template literals can also build HTML strings from task data:
const taskName = "Python exercise";
const row = `<tr><td>${taskName}</td></tr>`;
Why it is useful: It makes it easier to build strings that contain changing task information.
Security note: Do not insert untrusted user input into innerHTML without appropriate protection. This can create cross-site scripting (XSS) vulnerabilities. For plain user text, textContent or safe DOM element creation is generally preferable.
Documentation: MDN — Template literals
3.5 The Date Object — Checking Deadlines
JavaScript's Date object represents dates and times. Deskload can compare a task's due date with today's date to determine its status.
Example:
const today = new Date();
console.log(today);
A task manager may use these rules:
- Overdue: The due date has passed and the task is not complete.
- Due today: The task's due date is today.
- Upcoming: The due date is in the future.
Care is needed when comparing date strings, time zones, and times of day. Otherwise, a task may receive the wrong status.
Documentation: MDN — Date
3.6 DOM Manipulation — Updating the Page
The DOM (Document Object Model) represents a webpage as objects that JavaScript can access and change.
Example HTML:
<p id="message">No tasks yet.</p>
Select the element and update its text:
const message = document.getElementById("message");
message.textContent = "Task added successfully!";
Deskload can use DOM manipulation to:
- Display new tasks
- Update task status
- Refresh statistics
- Show an empty-state message
What is innerHTML?
innerHTML reads or sets the HTML markup inside an element. Setting it can replace the element's existing contents.
document.getElementById("task-list").innerHTML =
  "<p>HTML activity</p>";
Use care with user-provided text because untrusted HTML can create security problems.
What are event handlers?
Event handlers run code in response to events, such as a button click or checkbox change.
button.addEventListener("click", function () {
  console.log("Button clicked!");
});
Documentation: MDN — Document Object Model
3.7 try...catch — Error Handling
try...catch lets JavaScript respond to certain errors instead of allowing them to go unhandled.
Example:
try {
  const tasks = JSON.parse(
    localStorage.getItem("tasks") || "[]"
  );

  console.log(tasks);
} catch (error) {
  console.error("Unable to load tasks.", error);
}
- try contains code that may throw an error.
- catch runs if an error is thrown in the try block.
In Deskload, this can help handle invalid saved JSON or storage operations that fail.
Important: try...catch does not automatically fix every storage problem. The application should also decide what to do when saved data cannot be loaded or written.
Documentation: MDN — try...catch
4. Design and Typography
Google Fonts — Source Serif 4 and IBM Plex Sans
Typography refers to how text is styled and presented. Deskload's listed fonts are:
- Source Serif 4 for headings
- IBM Plex Sans for body text
A font can be loaded from Google Fonts using a link in the HTML <head>.
Example:
<link
  href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans&display=swap"
  rel="stylesheet"
>
Then use it in CSS:
body {
  font-family: "IBM Plex Sans", sans-serif;
}
Using different fonts for headings and body text can create visual hierarchy and improve readability. A fallback font should be specified in case the web font cannot load.
Official resource: Google Fonts
5. Concepts for Future Development
These concepts can help if Deskload grows from a browser-only demo into a larger application. They are not proof that the current demo already implements them.
5.1 Object-Oriented Programming (OOP)
OOP organizes code around objects and classes. A class acts as a blueprint for creating objects.
Example:
class Task {
  constructor(title, subject, dueDate) {
    this.title = title;
    this.subject = subject;
    this.dueDate = dueDate;
    this.completed = false;
  }

  markCompleted() {
    this.completed = true;
  }
}

const task = new Task(
  "Finish assignment",
  "CIT 742",
  "2026-10-20"
);

task.markCompleted();
- class Task defines the blueprint.
- constructor() initializes a new task.
- this.title and other properties store task information.
- markCompleted() is a method that changes the completion status.
- new Task(...) creates a new instance.
Encapsulation means grouping related data and behavior and controlling how data is accessed or changed.
Interfaces define a contract for operations a component should support. Plain JavaScript does not have TypeScript-style native interface declarations, but interfaces can be documented or implemented through conventions and other patterns.
For example, a TaskRepository could provide operations such as save(), findById(), and delete(). A TaskService could handle application rules.
Why it is useful: Separating responsibilities can make a larger application easier to test, maintain, and expand.
5.2 REST API Design
REST is an architectural style commonly used to design web services. A REST-style API can connect the Deskload front end to a backend service.
In a browser-only demo, JavaScript may save data directly to localStorage. In a backend version, the front end could send HTTP requests to a server, which validates and stores data in a database.
Example endpoint design:
HTTP method	Endpoint	Purpose
GET	/tasks	Retrieve the task list
GET	/tasks/1	Retrieve one task
POST	/tasks	Create a task
PUT	/tasks/1	Replace or update a task
DELETE	/tasks/1	Delete a task


Example request:
POST /tasks
Content-Type: application/json
{
  "title": "Finish CIT 742",
  "subject": "Multimedia Technology",
  "completed": false
}
A backend could validate the request and save the task in a database.
Potential benefits:
- Centralized task data
- Access from multiple devices when accounts and server storage are implemented
- A clear separation between the front end and business logic
- A place to implement authentication, authorization, and validation
A REST API alone does not provide these features automatically; the backend must implement them.
Documentation: MDN — REST
5.3 Progressive Web Apps (PWA)
A Progressive Web App is a web application that can provide app-like capabilities, such as installation and offline experiences, when the necessary features are implemented.
Two important parts are the web app manifest and service worker.
Web App Manifest
The manifest is a JSON file containing information about the application, such as its name, icons, and preferred display mode.
Example:
{
  "name": "Deskload",
  "short_name": "Deskload",
  "start_url": "/",
  "display": "standalone"
}
Browsers use manifest information as part of the installation experience. Exact installability requirements vary by browser and platform.
Service Worker
A service worker is a JavaScript worker that can handle events such as network requests. It can be used to cache application resources and support certain offline experiences.
For example, cached files may allow parts of Deskload to load without an internet connection after the user has visited the application. Offline task editing and later synchronization require additional implementation.
How PWA features differ from localStorage:
- localStorage stores string data such as task records.
- A service worker can handle network events and work with caching APIs.
- A manifest describes the application for installation-related behavior.
Important: A viewport tag or localStorage alone does not make an application a PWA.
Documentation: MDN — Progressive Web Apps
6. How the Technologies Work Together
A simplified view of Deskload:
1. HTML defines the forms, buttons, headings, and task list.
2. CSS styles the interface and adapts the layout to different screen sizes.
3. JavaScript handles task operations and updates the interface.
4. DOM APIs and event handlers connect user actions to changes on the page.
5. Array methods and the Date object help organize tasks and evaluate deadlines.
6. JSON and localStorage can preserve task data in the browser.
7. OOP, a REST API, and a database could be introduced in a future backend architecture.
8. PWA features could be added to support installation and selected offline behaviors.
Simple Architecture Diagram
User
 |
 v
Deskload Interface
(HTML + CSS)
 |
 v
JavaScript Application Logic
(Task operations, dates, arrays, DOM)
 |
 v
Browser Storage
(localStorage + JSON)

Possible future architecture:

Deskload Front End
 |
 | HTTP requests
 v
Task Service / REST API
 |
 v
Database
The browser-storage version and the future backend version are different architectures. Do not describe the REST API or database as implemented unless the source code confirms it.
7. References
The following official documentation links support the technologies discussed in this guide.
Core languages
- HTML — https://developer.mozilla.org/en-US/docs/Web/HTML
- CSS — https://developer.mozilla.org/en-US/docs/Web/CSS
- JavaScript — https://developer.mozilla.org/en-US/docs/Web/JavaScript
CSS
- CSS Custom Properties — https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties
- prefers-color-scheme — https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme
- Flexbox — https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout
- CSS Grid — https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout
- Media Queries — https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries
- Viewport Meta Tag — https://developer.mozilla.org/en-US/docs/Web/HTML/Guides/Viewport_meta_element
JavaScript and Web APIs
- localStorage — https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage
- Web Storage API — https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API
- JSON — https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON
- Array — https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array
- Template Literals — https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals
- Date — https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date
- DOM — https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model
- try...catch — https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch
Design and future development
- Google Fonts — https://fonts.google.com/
- REST — https://developer.mozilla.org/en-US/docs/Glossary/REST
- Progressive Web Apps — https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps
