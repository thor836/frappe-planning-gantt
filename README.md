<div align="center">    
    <h2>Planning Gantt</h2>
    <p>Based on <a href="https://github.com/frappe/gantt">Frape Gantt</a></p>    
</div>

Added support for categories and tasks combination per category.

### Install
```
npm install frappe-gantt
```

### Usage
Include it in your HTML:
```
<script src="frappe-gantt.min.js"></script>
<link rel="stylesheet" href="frappe-gantt.css">
```

And start hacking:
```js
var tasks = [
			{
				name: "Category 1",
				items: [{
					start: '2018-10-01',
					end: '2018-10-08',
					name: 'Jhon Doe 01',
					id: "Task 01",
				},{
					start: '2018-10-10',
					end: '2018-10-28',
					name: 'Jhon Doe 02',
					id: "Task 02",
				},{
					start: '2018-11-05',
					end: '2018-12-11',
					name: 'Jhon Doe 03',
					id: "Task 03",
				}]
			},
			{
				name: "Category 2",
				items: [{
					start: '2018-10-03',
					end: '2018-10-16',
					name: 'Donald Duck',
					id: "Task 1",
					progress: 0,
				}]
			},
			{
				name: 'Category 3'
			},
		]
var gantt = new Gantt("#gantt", tasks);
```

You can also pass various options to the Gantt constructor:
```js
var gantt = new Gantt("#gantt", tasks, {
    header_height: 50,
    column_width: 30,
    step: 24,
    view_modes: ['Quarter Day', 'Half Day', 'Day', 'Week', 'Month'],
    bar_height: 20,
    bar_corner_radius: 3,
    arrow_curve: 5,
    padding: 18,
    view_mode: 'Day',
    date_format: 'YYYY-MM-DD',
    language: 'en', // or 'es', 'it', 'ru', 'ptBr', 'fr', 'tr', 'zh', 'de', 'hu'
    custom_popup_html: null
});
```

### Contributing
If you want to contribute enhancements or fixes:

1. Clone this repo.
2. `cd` into project directory
3. `yarn`
4. `yarn run dev`
5. Open `index.html` in your browser, make your code changes and test them.

License: MIT

------------------
Project maintained by [frappe](https://github.com/frappe)
