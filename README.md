<html>
<head>
  <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
  <script type="text/javascript">
 google.charts.load('current', {packages: ['corechart', 'bar']});
google.charts.setOnLoadCallback(drawBasic);

function drawBasic() {

        var data = google.visualization.arrayToDataTable([
         ['Element', 'Conquistado', { role: 'style' }],
         ['Absoluto SM', 35, 'blue'],            // RGB value
         ['Meta Sup M', 100, 'red'],            // English color name
         ['ABS CC', 22, 'blue'],
         ['Meta CC', 100, 'red' ], // CSS-style declaration
      ]);

      var options = {
        title: 'Vamos pra cima familia absoluto!',
        chartArea: {width: '50%'},
        hAxis: {
          title: 'Meta',
          minValue: 0
        },
        vAxis: {
          title: ''
        }
      };

      var chart = new google.visualization.BarChart(document.getElementById('chart_div'));

      chart.draw(data, options);
    }
  </script>
  
  <script type="text/javascript">
  google.charts.load('current', {packages: ['corechart', 'bar']});
google.charts.setOnLoadCallback(drawStacked);

function drawStacked() {
      var data = google.visualization.arrayToDataTable([
        ['Absoluto','Sup SM','META','ABS CC'],
        ['CC/ Sup SM', 35,0,22],
		['META', 0, 100, 0],
    
      ]);

      var options = {
        title: 'Meta Corporativa',
        chartArea: {width: '50%'},
        isStacked: true,
        hAxis: {
          title: 'Volume',
          minValue: 0,
        },
        vAxis: {
          title: ''
        }
      };
      var chart = new google.visualization.BarChart(document.getElementById('chart_div2'));
      chart.draw(data, options);
    }
  
  </script>
</head>
<body>
	<center><img src="logo.png" alt="Girl in a jacket" ></center>
  <div id="chart_div"></div>
    <div id="chart_div2"></div>
</body>
</html>
