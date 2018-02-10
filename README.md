# Java-Script-API

## Supports

* Element styles with css syntax
* Create HTML elements with their attributes
* Get/Set html and attribute value
* Bind one or multiple events

## Functions

```javascript

J$(element).append(elementTagName, ebjectOfAttributes, numberOfElements)

J$(element).css(objectOfCssStyles)

J$(element).val(value)

J$(element).html(html)

J$(element).on(eventName, function)

```


## How to include in my document?
```html
<script type="text/javascript" src="https://bichiko.github.io/JavaScript-API/script.js"></script>
```
* Copy/Paste inside your `<head>` and you are ready to go! *

<hr>
## Examples

### Code#1
```javascript
J$('body').append('input');
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
<hr>

### Code#2
```javascript
J$('body').append('input',{
	'value':'new one',
	'type':'text',
	'class':'mylcass',
	'name':'myname',
	'id':'myid',
	'data-val':'someval'
}).css({
	'padding':'10px 20px',
	'margin':'5px 10px',
	'color':'rgba(255,0,0,0.6)'
});
```


### Result
```html
<body>
	<input value="new one" type="text" class="mylcass" name="myname" id="myid" data-val="someval" style="padding: 10px 20px; margin: 5px 10px; color: rgba(255, 0, 0, 0.6);">
</body>
```

<hr>

### Code#4
```javascript
var outerDiv = J$('body').append('div')
var buttons = J$(outerDiv.child).append('button', 2).html('<b>Click me!</b>')

//or
var outerDiv = J$('body').append('div')
	,buttons = J$(outerDiv.child).append('button', 2).html('<b>Click me!</b>')
```


### Result
```html
<body>
	<div>
		<button>
			<b>Click me!</b>
		</button>
		<button>
			<b>Click me!</b>
		</button>
	</div>
</body>
```