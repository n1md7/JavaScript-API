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
* Copy/Paste script below inside your `<head>` and you are ready to go! *
```html
<script type="text/javascript" src="https://bichiko.github.io/JavaScript-API/script.js"></script>
```

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



<hr>

### Code#5
```javascript
var container = J$('body').append('div',{'class':'container'}).css({
		'position':'relative',
		'margin':'auto',
		'width':'100%',
		'border':'solid 1px rgba(255,0,0,0.2)',
		'border-radius':'3px',
		'box-sizing':'border-box',
		'padding':'20px 40px',
		'overflow':'auto'
	}),table = J$(container.child).append('table', { 'border':'1', 'style':'width:100%;' })
	  ,tr = J$(table.child).append('tr',5)
	  ,td = J$(tr.child).append('td',4, {'contentEditable':'true'})
	  	.html('Default Value').css({
		  	'width':'80px',
		  	'text-align':'center',
		  	'font-weight':'bold',
		  	'color':'rgba(255,0,0,0.3)',
		  	'padding':'5px 10px',
		  	'cursor':'pointer',
		  	'transition':'all 0.3s'
		  }).on('mouseover', function(){
		  	J$(this).css({
		  		'color':'red',
		  		'border':'solid 1px red',
		  		'background':'rgba(0,0,0,0.1)'
		  	})
		  }).on('mouseout', function(){
		  	J$(this).css({
		  		'color':'rgba(255,0,0,0.3)',
		  		'border':'1px solid black',
		  		'background':'rgba(0,0,0,0.0)'
		  	})
		  }).on('keydown', function(event){
		  	switch(event.keyCode){
		  		case 9 : J$(this).html('[Tab]');
		  			event.preventDefault(); break
		  		case 13: J$(this).html('[Enter]');
		  			event.preventDefault(); break
		  	}
		  })
```


### Result Demo
<iframe src="https://bichiko.github.io/JavaScript-API/demo.html" frameborder="0" ></iframe>