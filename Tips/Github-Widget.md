# Github contiribute widget 추가하기

## Javascript in Html
```html
<!-- Include the library. -->
<script
  src="https://unpkg.com/github-calendar@latest/dist/github-calendar.min.js"
></script>

<!-- Optionally, include the theme (if you don't want to struggle to write the CSS) -->
<link
   rel="stylesheet"
   href="https://unpkg.com/github-calendar@latest/dist/github-calendar-responsive.css"
/>

<!-- Prepare a container for your calendar. -->
<div class="calendar">
    <!-- Loading stuff -->
    Loading the data just for you.
</div>

<script>
    GitHubCalendar(".calendar", "your-username");
    // or enable responsive functionality
    GitHubCalendar(".calendar", "your-username", { responsive: true });
</script>
```

## CSS
```css
.calendar-graph text.wday,
.calendar-graph text.month {
    font-size: 10px;
    fill: #aaa;
}

.contrib-legend {
    text-align: right;
    padding: 0px;
    display: none;
    float: right;
}

.contrib-legend .legend {
    display: inline-block;
    list-style: none;
    margin: 0 5px;
    position: relative;
    bottom: -1px;
    padding: 0;
}

.contrib-legend .legend li {
    display: inline-block;
    width: 10px;
    height: 10px;
}

.text-small {
    font-size: 12px;
    color: #767676;
}

.calendar-graph {
    padding: 5px 0 0;
    text-align: center;
}

.contrib-column {
    padding: 15px 0;
    text-align: center;
    border-left: 1px solid #ddd;
    border-top: 1px solid #ddd;
    font-size: 11px;
}

.contrib-column-first {
    border-left: 0;
}

.table-column {
    display: none;
    width: 1%;
    padding-right: 10px;
    padding-left: 10px;
    vertical-align: top;
}

.contrib-number {
    font-weight: 300;
    line-height: 1.3em;
    font-size: 24px;
    display: block;
    color: #333;
}

.calendar img.spinner {
    width: 70px;
    margin-top: 50px;
    min-height: 70px;
}

.monospace {
    text-align: center;
    color: #000;
    font-family: monospace;
}

.monospace a {
    color: #1D75AB;
    text-decoration: none;
}

.contrib-footer {
    font-size: 11px;
    padding: 0 10px 12px;
    text-align: left;
    width: 100%;
    box-sizing: border-box;
    height: 26px;
}

.left.text-muted {
    float: left;
    margin-left: 9px;
    color: #767676;
}
.left.text-muted a {
    color: #4078c0;
    text-decoration: none;
}
.left.text-muted a:hover,
.monospace a:hover {
    text-decoration: underline;
}

h2.f4.text-normal.mb-3 {
    display: none;
}

.float-left.text-gray {
    float: left;
}
#user-activity-overview{
    display:none;
}
```

## Result
![result](https://github.com/Atelier-de-Orca/tistory-tips/blob/master/Resources/Github-Widget.PNG)
