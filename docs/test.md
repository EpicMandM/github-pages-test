---
title: Chart Example
---
<div style="width: 50%">
  <canvas id="myChart" height="450" width="600"></canvas>
</div>

<script>
<!-- Load Chart.js library -->
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<!-- Chart container -->
<div style="width: 50%">
  <canvas id="myChart" height="450" width="600"></canvas>
</div>

<!-- Chart script -->
<script>
function getRandomDataArray() {
  var dataArray = [];
  for (var i = 0; i < 7; i++) {
    dataArray.push(Math.round(Math.random() * 100));
  }
  return dataArray;
}

var chartData = {
  labels: ["January", "February", "March", "April", "May", "June", "July"],
  datasets: [
    {
      label: "My First dataset",
      backgroundColor: "rgba(220,220,220,0.2)",
      borderColor: "rgba(220,220,220,1)",
      pointBackgroundColor: "rgba(220,220,220,1)",
      pointBorderColor: "#fff",
      pointHoverBackgroundColor: "#fff",
      pointHoverBorderColor: "rgba(220,220,220,1)",
      data: getRandomDataArray(),
      fill: true,
    },
    {
      label: "My Second dataset",
      backgroundColor: "rgba(151,187,205,0.2)",
      borderColor: "rgba(151,187,205,1)",
      pointBackgroundColor: "rgba(151,187,205,1)",
      pointBorderColor: "#fff",
      pointHoverBackgroundColor: "#fff",
      pointHoverBorderColor: "rgba(151,187,205,1)",
      data: getRandomDataArray(),
      fill: true,
    },
  ],
};

window.onload = function () {
  var ctx = document.getElementById("myChart").getContext("2d");
  var myLineChart = new Chart(ctx, {
    type: "line",
    data: chartData,
    options: {
      responsive: true,
    },
  });
};
</script>
