# Uncommon HTML Bug: Event Listener on Removed Element

This repository demonstrates an uncommon bug in HTML that can occur when an event listener is attached to an element that's dynamically removed from the DOM.  The bug results in an error because JavaScript attempts to access an element that no longer exists.

## Bug Description
The primary issue lies in the `myFunction()` function. It removes the content of the div with the id "myDiv", but it does not remove the event listener attached to that same div. When the button is clicked again, the code attempts to use `document.getElementById("myDiv")` which now returns null as the element has been removed, leading to an error.

## Solution
The solution involves removing the event listener before the element is removed or modified. This prevents JavaScript from attempting to interact with a non-existent element.  The updated code shows how to do this effectively.