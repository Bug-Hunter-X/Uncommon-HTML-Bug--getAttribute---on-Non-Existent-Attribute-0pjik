# Uncommon HTML Bug: Silent Failure of getAttribute()

This repository demonstrates a subtle bug related to the `getAttribute()` method in JavaScript when used with HTML elements.

## The Bug

When you attempt to retrieve the value of a non-existent attribute using `getAttribute()`, instead of throwing an error, it silently returns `null`.  This can lead to unexpected behavior, especially if your code doesn't explicitly check for this `null` value.

## Reproduction

1. Open `bug.html` in a web browser.
2. Observe the console output. You'll see a `null` value logged for the non-existent attribute.
3. Uncomment the last line in the `<script>` tag to see how the more common error of accessing a non-existent element behaves.

## Solution

The best practice is always to check if `getAttribute()` returns `null` before using the returned value. The solution provided shows how to handle this case gracefully. 

## Note

This bug highlights the importance of robust error handling in JavaScript when working with the DOM.