1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

getElementById is used when I want to select one specific element using its id. Since id is unique, it always returns only one element.
getElementsByClassName is used when I want to select multiple elements that have the same class name. It returns a collection of elements.
querySelector works like CSS selector. It selects the first matching element.
querySelectorAll also works like CSS selector, but it selects all matching elements.

So, getElementById is for one unique element, getElementsByClassName is for multiple elements by class, querySelector gives first match, 
and querySelectorAll gives all matches.


2. <--------------How do you create and insert a new element into the DOM?------------------>

First, I create a new element using document.createElement().
Then I add text or content inside it.
After that, I insert it into the DOM using append() or appendChild().

Example:
const newDiv = document.createElement("div");
newDiv.innerText = "Hello World";
document.body.appendChild(newDiv);

3 <----------What is Event Bubbling? And how does it work?------------------------>

Event bubbling means when an event happens on a child element, it first runs on that element and then moves up to its parent elements.
For example, if a button is inside a div and I click the button:
First, the button’s click event runs
Then, the div’s click event runs
This upward movement of the event is called event bubbling.

4.##### What is Event Delegation in JavaScript? Why is it useful?#########------------------>

Event delegation means adding one event listener to a parent element instead of adding separate listeners to each child.
The parent handles events for its children.

It is useful because:
It reduces code
It improves performance
It works even if new elements are added later

5.<-------- What is the difference between preventDefault() and stopPropagation() methods?--------------->

preventDefault() is used to stop the browser’s default behavior.
For example, stopping a form from reloading the page when submitted.
stopPropagation() is used to stop the event from moving up to parent elements.
It stops event bubbling.

So, preventDefault() stops default browser action, and stopPropagation() stops event bubbling.
