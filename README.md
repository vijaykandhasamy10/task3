# task3
1.With JSON using For IN loop:

var res={
  "name":"vijay",
  "age":"22"
}
for(var a in res){
  console.log(a,res[a]);
}

Using FOR loop:

var res={
  "name":"vijay",
  "age":"22"
}
for(var res){
  console.log(res.name);
};

Using FOR OF loop:
var marks=[90,80,48,70]
for(var list of marks){
  console.log(list);
};
2.Using JSON to create own resume

let myResume={
    "basics": {
      "name": "vijay kandhasamy p",
      "email": "ilanjivijaykandhasamy.10@gamil.com",
      "phone": 9952793982,
      "degree": "B.E",
    },
      "location": {
        "address": "41,juubliee road ilanji",
        "postalCode": 627805,
        "city": "Tenkasi",
        "state": "Tamilnadu",
        "country": "India"
      },
    "education": [
      {
        "institution": "Hindusthan college of engineering and technology",
        "department": "EEE",
        "studyType": "fulltime",
        "batch start year": 2019,
        "batch end year": 2022,
        "gpa": 7.9,
      }
    ],
    "skills": [
      {
        "name": "python,javascript,java,html,edito",
        "level": "intermediate",
      }
    ],
    "languages": [
      {
        "language": "Tamil,Enlish",
      }
    ],
    "interests": [
      {
        "name": "travelling,gamer",
      }
    ]
  }
  console.log(myResume);

4.Difference between Window,Screen and Object;

•	WINDOW is the execution context and global object for that context's JavaScript.
•	DOCUMENT contains the DOM, initialized by parsing HTML.

•	SCREEN describes the physical display's full screen.

WINDOW:

Each browser tab has its own top-level window object. Each <iframe> (and deprecated <frame>) element has its own window object too, nested within a parent window. Each of these windows gets its own separate global object. 

window.window always refers to window, but window.parent and window.top might refer to enclosing windows, giving access to other execution contexts. In addition to document and screen described below, window properties include

•	setTimeout() and setInterval() binding event handlers to a timer
•	location giving the current URL
•	history with methods back() and forward() giving the tab's mutable history
•	navigator describing the browser software

DOCUMENT:

Each window object has a document object to be rendered. These objects get confused in part because HTML elements are added to the global object when assigned a unique id. E.g., in the HTML snippet

<body>
  <p id="holyCow"> This is the first paragraph.</p>
</body>
the paragraph element can be referenced by any of the following:

•	window.holyCow or window["holyCow"]
•	document.getElementById("holyCow")
•	document.querySelector("#holyCow")
•	document.body.firstChild
•	document.body.children[0]

SCREEN:

The window object also has a screen object with properties describing the physical display:

•	screen properties width and height are the full screen

•	screen properties availWidth and availHeight omit the toolbar

The portion of a screen displaying the rendered document is the viewport in JavaScript, which is potentially confusing because we call an application's portion of the screen a window when talking about interactions with the operating system. 

The getBoundingClientRect() method of any document element will return an object with top, left, bottom, and right properties describing the location of the element in the viewport.
