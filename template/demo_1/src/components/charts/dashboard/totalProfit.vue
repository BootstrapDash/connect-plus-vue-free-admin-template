<script>
import {
  Line
} from 'vue-chartjs'

export default {
  name: 'totalProfit',
  extends: Line,
  data () {
    return {
      totalProfitData: {
        labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep"],
				datasets: [{
					label: 'Margin',
					data: [5, 4, 6, 4.5, 5.5, 4, 5, 4.2, 5.5],
					backgroundColor: [
						'#cfe1ff',
					],
					borderColor: [
						'#0062ff'
					],
					borderWidth: 3,
					fill: true,
				}],
      },
      totalProfitOptions: {
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
    this.renderChart(this.totalProfitData, this.totalProfitOptions)
  }
}
</script>
