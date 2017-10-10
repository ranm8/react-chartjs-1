rich interactive react Line chart component using chart.js.
for more Info go to [chart.js](http://www.chartjs.org/) 

```js
Chart.defaults.global.responsive = true;

var LineChart = require("react-chartjs").Line;

var MyComponent = React.createClass({
  render: function() {
    return <LineChart data={chartData} options={chartOptions}/>
  }
});
```

* ```data``` represents the chart data (see [chart.js](http://www.chartjs.org/) for details)
* ```options``` represents the chart options (see [chart.js](http://www.chartjs.org/) for details)
* all other parameters will be passed through to the ```canvas``` element
* if data passed into the component changes, points will animate between values using chart.js' ```.update()```. If you want the chart destroyed and redrawn on every change, pass in ```redraw``` as a prop. For example ```<LineChart data={this.state.chartData} redraw />```

Chart References
----------------
The ```canvas``` element can be retrieved using ```getCanvas``` and the ```chartjs object``` can be retrieved using ```getChart```.