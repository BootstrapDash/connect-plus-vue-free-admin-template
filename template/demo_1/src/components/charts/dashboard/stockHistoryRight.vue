<script lang='js'>
import {
  Line
} from 'vue-chartjs'
export default {
  extends: Line,
  props: {
    labels: {
      type: Array,
      default: () => ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul"]
    }
  },
  data () {
    return {
      gradient: null,
      gradient2: null
    }
  },
  mounted () {
    this.gradient = this.$refs.canvas.getContext('2d').createLinearGradient(25, 0, 25, 80)
    this.gradient.addColorStop(0, '#0062ff')
    this.gradient.addColorStop(1, 'rgba(255, 255, 255, 0.27)')
    this.renderChart({
      labels: this.labels,
      datasets: [{
        label: 'CHN',
        data: [3, 2, 1, 3, 2, 4, 3],
        borderColor: "#0062ff",
        backgroundColor: this.gradient,
        borderWidth: 3
      }]
    }, {
      responsive: true,
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
          tension: .4
        }
      },
      tooltips: {
        backgroundColor: 'rgba(2, 171, 254, 1)',
      },
    })
  }
}
</script>

<style scoped lang='scss'>
  .visitAndSalesStatitics {
  }
</style>
