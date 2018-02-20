# Reference links:

1. full list of DOM specs: https://www.w3.org/standards/techs/dom#w3c_all

2. MDN on getElementById and getElementsByClassName

3. EVERY NODE PROPERTIES AND METHODS YOU CAN CALL ON GETELEMENTBYID: https://developer.mozilla.org/en-US/docs/Web/API/Node

4. LIST OF WEB APIs: https://developer.mozilla.org/en-US/docs/Web/API



# How to operate on the dom

### Get element by ID (return single)

document.getElementById('footer');

### Get element by class (return mutliple)

.getElementsByClassName()
.getElementsByTagName()


### What they return

A HTML collection (NOT AN ARRAY!)


### Queryselectors (one)

// find and return the element with an ID of "header"
document.querySelector('#header');

// find and return the first element with the class "header"
document.querySelector('.header');

// find and return the first <header> element
document.querySelector('header');


### Queryselector (all)

// find and return a list of elements with the class "header"
document.querySelectorAll('.header');

// find and return a list of <header> elements
document.querySelectorAll('header');


### Update Existing Page Content

`.innerHTML`: will get/set an element's HTML content
`.textContent`: set/get text content of an element and all its decendants
`.innerText`: returns the text as it would be seen visually (with css)

### Add New Page Content

`document.createElement()`: Method that create element (does not add it to DOM)

How you add as last child'.appendChild()':
// create a brand new <span> element
const newSpan = document.createElement('span');

// select the first (main) heading of the page
const mainHeading = document.querySelector('h1');

// add the the <span> element as the last child element of the main heading
mainHeading.appendChild(newSpan);



How to add elsewhere:

`.insertAdjacentHTML()`: needs two arguments 1. the location of HTML and 2 the HTML text that is going to be inserted. The arguments for placement:

<!-- beforebegin -->
<p>
    <!-- afterbegin -->
    Existing text/HTML content
    <!-- beforeend -->
</p>
<!-- afterend -->


### Remove Page Content

`.removeChild()`: remove child element. req: 1. a parent element 2. the child element that will be removed

`<parent-element>.removeChild(<child-to-remove>);`

Example:
const mainHeading = document.querySelector('h1');
mainHeading.parentElement.removeChild(mainHeading);


THE BEST WAY:

`.remove()`

How:

const mainHeading = document.querySelector('h1');
mainHeading.remove();


### Styling Page Content

One at a time:
mainHeading.style.color = 'red';

Multiple:
mainHeading.style.cssText = 'color: blue; background-color: orange; font-size: 3.5em';

Set attribute to an element:
mainHeading.setAttribute('style', 'color: blue; background-color: orange; font-size: 3.5em;');

BEST WAY: Let CSS do the CSS job, and let JS only change the classname:

mainHeading.className = "im-the-new-class";
"The above code erases any classes that were originally in the element's class attribute and replaces it with the single class im-the-new-class."



You might need to store class names: BY FAR THE MOST POWERFUL OF ALL THESE IN STYLING PAGE CONTENT SECTION!

const mainHeading = document.querySelector('#main-heading');

// store the list of classes in a variable
const listOfClasses = mainHeading.classList;

// logs out ["ank-student", "jpk-modal"]
console.log(listOfClasses);

classList properties:
.add() .remove() .toggle() .contains()


######### RESPOND TO EVENTS #########

### Monitor events (for developement only)

// start displaying all events on the document object
monitorEvents(document);

// turn off the displaying of all events on the document object.
unmonitorEvents(document);

https://developers.google.com/web/tools/chrome-devtools/console/events#monitor_events

### Event Target

EventTarget interface only has three methods (and zero properties)

.addEventListener()
.removeEventListener()
.dispatchEvent()


### Adding An Event Listener

.addEventListener(): Listen for events and respond to them

<event-target>.addEventListener(<event-to-listen-for>, <function-to-run-when-an-event-happens>);


The <event-target> (i.e. the target) goes right back to what we just looked at: everything on the web is an event target (e.g. the document object, a <p> element, etc.).

The <event-to-listen-for> (i.e. the type) is the event we want to respond to. It could be a click, a double click, the pressing of a key on the keyboard, the scrolling of the mouse wheel, the submitting of a form...the list goes on!

The <function-to-run-when-an-event-happens> (i.e. the listener) is a function to run when the event actually occurs.


EXAMPLE:

const mainHeading = document.querySelector('h1');

mainHeading.addEventListener('click', function () {
  console.log('The heading was clicked!');
});

doc: https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener


List of events to listen to: https://developer.mozilla.org/en-US/docs/Web/Events



### Removing an Event Listener

.removeEventListener() method requires you to pass the same exact listener function to it as the one you passed to .addEventListener().


`<event-target>.removeEventListener(<event-to-listen-for>, <function-to-remove>);`

### Running javascript in the <head> section

You listen to when the DOM is finished:
<script>
      document.addEventListener('DOMContentLoaded', function () {
          document.querySelector('footer').style.backgroundColor = 'purple';
      });
</script>

So when would you want to use this technique?

Well, JavaScript code in the <head> will run before JavaScript code in the <body>, so if you do have JavaScript code that needs to run as soon as possible, then you could put that code in the <head> and wrap it in a DOMContentLoaded event listener. This way it will run as early as possible, but not too early that the DOM isn't ready for it.


### Phases of an event

3 phases: capturing, at target and bubbling

prevent default action: .preventDefault()



# LINKS

- [Listen for click over multiple (iterable) elements - We need to use closure!](https://zerobin.net/?01bf091c3495bc3c#LnVFBsPm56opImSiIf5t/vnTfR36bl1bMzbgOGHNCIk=)
