# Java-Script-API

## Supports

* Element styles with css syntax
* Create HTML elements with their attributes
* Get/Set html and attribute value
* Bind one or multiple events

## Functions

```javascript

J$(element/object).append(elementTagName, ebjectOfAttributes, numberOfElements)

J$(element/object).css(objectOfCssStyles)

J$(element/object).val(value)

J$(element/object).html(html)

J$(element/object).on(eventName, function)

```

## Examples

### Code
```javascript
// Example#1
J$('body').append('input');
// Example#2
J$(document.body).append('input');
```

## Results

### Before
```html
<body>
</body>
```

### After
```html
<body>
	<input>
</body>
```