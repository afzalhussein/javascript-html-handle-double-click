# javascript-html-handle-double-click

To handle a double click event in HTML, you can use the `ondblclick` event attribute or the `addEventListener` method with the "dblclick" event type. Here's a step-by-step guide with examples for both approaches:

### Method 1: Using `ondblclick` Event Attribute

1. Create an HTML element that you want to respond to a double click event. For example, let's use a `<button>` element:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Double Click Example</title>
</head>
<body>
    <button id="myButton" ondblclick="handleDoubleClick()">Double Click Me</button>

    <script>
        function handleDoubleClick() {
            alert('Double clicked!');
        }
    </script>
</body>
</html>
```

In this example, the `ondblclick` event attribute is set to call the `handleDoubleClick` function when the button is double-clicked. The function displays an alert message.

### Method 2: Using `addEventListener` with "dblclick" Event Type

1. Create an HTML element as before, but without the `ondblclick` attribute:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Double Click Example</title>
</head>
<body>
    <button id="myButton">Double Click Me</button>

    <script>
        var button = document.getElementById('myButton');

        button.addEventListener('dblclick', function() {
            alert('Double clicked!');
        });
    </script>
</body>
</html>
```

In this example, JavaScript is used to select the button element by its ID and then add an event listener for the "dblclick" event. The listener calls an anonymous function that displays an alert when a double click occurs on the button.

Both methods achieve the same result of handling a double click event, but the second method using `addEventListener` is generally preferred as it separates JavaScript from the HTML markup, making your code more maintainable and flexible.
