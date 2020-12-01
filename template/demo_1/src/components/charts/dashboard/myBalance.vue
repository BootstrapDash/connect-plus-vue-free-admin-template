<script>
import {
  Bar
} from 'vue-chartjs'

export default {
  extends: Bar,
  data () {
    return {
      datacollection: {
        labels: ["Jan", "Feb", "Mar", "Apr"],
				datasets: [{
						label: 'Demand',
						data: [90, 85, 100, 105],
						backgroundColor: [
							'#0062ff', '#0062ff', '#0062ff', '#0062ff',
						],
						borderColor: [
							'#0062ff', '#0062ff', '#0062ff', '#0062ff',
						],
						borderWidth: 1,
						fill: false
					},
					{
						label: 'Supply',
						data: [200, 200, 200, 200],
						backgroundColor: [
							'#eef0fa', '#eef0fa', '#eef0fa', '#eef0fa',
						],
						borderColor: [
							'#eef0fa', '#eef0fa', '#eef0fa', '#eef0fa',
						],
						borderWidth: 1,
						fill: false
					}
				]
      },
      options: {
        scales: {
					xAxes: [{
						stacked: true,
						barPercentage: .7,
						position: 'bottom',
						display: true,
						gridLines: {
							display: false,
							drawBorder: false,
							drawTicks: false
						},
						ticks: {
							display: true, //this will remove only the label
							stepSize: 500,
							fontColor: "#111",
							fontSize: 12,
							padding: 10,
						}
					}],
					yAxes: [{
						stacked: false,
						display: false,
						gridLines: {
							drawBorder: true,
							display: false,
							color: "#eef0fa",
							drawTicks: false,
							zeroLineColor: 'rgba(90, 113, 208, 0)',
						},
						ticks: {
							display: true,
							beginAtZero: true,
							stepSize: 200,
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
    this.renderChart(this.datacollection, this.options)
  }
}
</script>

<style scoped lang="scss">
  .bar-chart {} 
</style>
