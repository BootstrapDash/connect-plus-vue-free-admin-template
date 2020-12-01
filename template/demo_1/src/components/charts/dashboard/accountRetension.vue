<script>
import {
  Bar
} from 'vue-chartjs'

export default {
  name: 'totalExpence',
  extends: Bar,
  data () {
    return {
      totalExpenceData: {
        labels: ["Jan", "Feb", "Mar", "Apr", "May"],
				datasets: [{
						label: 'Demand',
						data: [33, 48, 39, 36, 36],
						backgroundColor: [
							'#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8',
						],
						borderColor: [
							'#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8',
						],
						borderWidth: 1,
						fill: false
					},
					{
						label: 'Demand',
						data: [94, 28, 49, 25, 20],
						backgroundColor: [
							'#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8',
						],
						borderColor: [
							'#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8',
						],
						borderWidth: 1,
						fill: false
					},
					{
						label: 'Demand',
						data: [66, 33, 25, 36, 69],
						backgroundColor: [
							'#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8',
						],
						borderColor: [
							'#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8', '#d8d8d8',
						],
						borderWidth: 1,
						fill: false
					}
				]
      },
      totalExpenceOptions: {
        scales: {
					xAxes: [{
						stacked: false,
						position: 'bottom',
						display: true,
						barPercentage: .7,
						categoryPercentage: 1,
						gridLines: {
							display: false,
							drawBorder: false,
							drawTicks: false
						},
						ticks: {
							display: true, //this will remove only the label
							stepSize: 500,
							fontColor: "#a7afb7",
							fontSize: 14,
							padding: 10,
						}
					}],
					yAxes: [{
						stacked: false,
						display: true,
						gridLines: {
							drawBorder: false,
							display: true,
							color: "#c31a56",
							drawTicks: false,
							zeroLineColor: 'rgba(90, 113, 208, 0)',
						},
						ticks: {
							display: false,
							beginAtZero: true,
							stepSize: 40,
							fontColor: "#a7afb7",
							fontSize: 14,

						},
					}]
				},
				legend: {
					display: false
				},
				tooltips: {
					backgroundColor: 'rgba(0, 0, 0, 1)',
				},
				plugins: {
					datalabels: {
						display: false,
						align: 'center',
						anchor: 'center'
					}
				}
      }
    }
  },
  mounted () {
    this.renderChart(this.totalExpenceData, this.totalExpenceOptions)
  }
}
</script>
