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
        labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep"],
				datasets: [{
					label: 'Margin',
					data: [4, 5, 6, 5, 4, 5, 4, 6, 5],
					backgroundColor: [
						'#e1fff3',
					],
					borderColor: [
						'#3dd597'
					],
					borderWidth: 3,
					fill: true,
				}],
      },
      totalExpenceOptions: {
        scales: {
					yAxes: [{
						display: false,
						gridLines: {
							drawBorder: false,
							display: false,
							drawTicks: false
						},
						ticks: {
							beginAtZero: true,
							stepSize: 10
						}
					}],
					xAxes: [{
						display: false,
						position: 'bottom',
						gridLines: {
							drawBorder: false,
							display: false,
							drawTicks: false
						},
						ticks: {
							beginAtZero: true,
							stepSize: 10
						}
					}],
				},
				legend: {
					display: false,
				},
				elements: {
					point: {
						radius: 0
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
