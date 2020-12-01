<script>
import {
  Line
} from 'vue-chartjs'

export default {
  name: 'totalExpence',
  extends: Line,
  data () {
    return {
      totalExpenceData: {
        labels: ["1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12", "13", "14", "15", "16", "17", "18", "19", "20", "21", "22", "23", "24", "25", "26", "27", "28"],
				datasets: [{
						label: 'This week',
						data: [46, 49, 51, 58, 63.61, 65, 64, 69, 70, 78, 80, 80, 90, 85, 87, 92, 97, 102, 107, 109, 111, 111, 120, 130, 132, 136, 140, 145],
						backgroundColor: [
							'rgba(216,247,234, 0.19)',
						],
						borderColor: [
							'#3dd597'
						],
						borderWidth: 2,
						fill: true,
						pointBorderColor: "#fff",
						pointBackgroundColor: "#3dd597",
						pointBorderWidth: 2,
						pointRadius: 4,
					},
					{
						label: 'Current week',
						data: [16, 19, 21, 28, 33.31, 35, 34, 39, 40, 48, 50, 50, 51, 55, 57, 62, 67, 69, 68, 70, 72, 75, 74, 80, 79, 80, 84, 90],
						backgroundColor: [
							'rgba(216,247,234, 0.19)',
						],
						borderColor: [
							'#3dd597'
						],
						borderWidth: 2,
						fill: false,
						pointBorderColor: "#fff",
						pointBackgroundColor: "#0162ff",
						pointBorderWidth: 2,
						pointRadius: 4,
					}
				],
      },
      totalExpenceOptions: {
        scales: {
					yAxes: [{
						display: true,
						gridLines: {
							drawBorder: false,
							display: true,
							drawTicks: false,
							color: '#eef0fa',
							zeroLineColor: 'rgba(90, 113, 208, 0)',
						},
						ticks: {
							beginAtZero: true,
							stepSize: 50,
							display: true,
							padding: 10,
						}
					}],
					xAxes: [{
						display: true,
						position: 'bottom',
						gridLines: {
							drawBorder: false,
							display: false,
							drawTicks: false,
						},
						ticks: {
							beginAtZero: true,
							stepSize: 10,
							fontColor: "#a7afb7",
							padding: 10,
						}
					}],
				},
				legend: {
					display: false,
				},
				elements: {
					point: {
						radius: 1
					},
					line: {
						tension: 0
					}
				},
				tooltips: {
					backgroundColor: 'rgba(2, 171, 254, 1)',
				},
      }
    }
  },
  mounted () {
    this.renderChart(this.totalExpenceData, this.totalExpenceOptions)
  }
}
</script>
