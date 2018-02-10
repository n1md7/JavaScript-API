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

### Code#3
```javascript
J$('body').append('input',3,{'type':'text'});
```


### Result
```html
<body>
	<input type="text">
	<input type="text">
	<input type="text">
</body>
```