<template>
  <section class="dashboard">
    <div class="proBanner">
      <div>
        <span class="d-flex align-items-center purchase-popup">
          <p>Get tons of UI components, Plugins, multiple layouts, 20+ sample pages, and more!</p>
          <a href="https://www.bootstrapdash.com/product/connect-plus-vue/?utm_source=organic&utm_medium=banner&utm_campaign=free-preview" rel="noopener noreferrer" target="_blank" class="btn btn-sm purchase-button ml-auto">Check Pro Version</a>
          <i class="mdi mdi-close bannerClose"  @click="toggleProBanner()" ></i>
        </span>
      </div>
    </div>
   <div class="d-xl-flex justify-content-between align-items-start">
      <h2 class="text-dark font-weight-bold mb-2"> Overview dashboard </h2>
      <div class="d-sm-flex justify-content-xl-between align-items-center mb-2">
        <div class="btn-group bg-white p-3" role="group" aria-label="Basic example">
          <button type="button" class="btn btn-link text-light py-0 border-right">7 Days</button>
          <button type="button" class="btn btn-link text-dark py-0 border-right">1 Month</button>
          <button type="button" class="btn btn-link text-light py-0">3 Month</button>
        </div>

        <b-dropdown id="ddown35" text="Dropdown" variant="white" class="bg-white ml-0 ml-md-4 mt-2 mt-lg-0 py-1 px-2">
          <template slot="button-content">
            <span class="py-3" id="calendarDrop" href="javascript:void(0);" data-toggle="dropdown" aria-expanded="false">
              <i class="mdi mdi-calendar mr-1"></i>24 Mar 2019 - 24 Mar 2019 
            </span>
          </template>
          <b-dropdown-item>Settings</b-dropdown-item>
          <b-dropdown-item>Action</b-dropdown-item>
          <b-dropdown-item>Another action</b-dropdown-item>
          <b-dropdown-divider></b-dropdown-divider>
          <b-dropdown-item>Something else here...</b-dropdown-item>
          <b-dropdown-item disabled>Disabled action</b-dropdown-item>
        </b-dropdown>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-12">
        <b-tabs class="tab-transparent">
          <b-tab title="Users" disabled>
            <div>
              Users
            </div>
          </b-tab>
          <b-tab title="Business" active>
            <div class="tab-transparent-content">
              <div class="row">
                <div class="col-xl-3 col-lg-6 col-sm-6 grid-margin stretch-card">
                  <div class="card">
                    <div class="card-body text-center">
                      <h5 class="mb-2 text-dark font-weight-normal">Orders</h5>
                      <h2 class="mb-4 text-dark font-weight-bold">932.00</h2>
                      <div>
                        <radial-progress-bar class="ml-auto mr-auto" :diameter="125"
                        :completed-steps="70"
                        :total-steps="100"
                        innerStrokeColor="#eee"
                        startColor = "#1579ff"
                        stopColor="#7922e5"
                        :strokeWidth="7"
                        >
                        <i class="mdi mdi-lightbulb icon-md absolute-center text-dark"></i>
                      </radial-progress-bar>
                      </div>
                      <p class="mt-4 mb-0">Completed</p>
                      <h3 class="mb-0 font-weight-bold mt-2 text-dark">5443</h3>
                    </div>
                  </div>
                </div>
                <div class="col-xl-3 col-lg-6 col-sm-6 grid-margin stretch-card">
                  <div class="card">
                    <div class="card-body text-center">
                      <h5 class="mb-2 text-dark font-weight-normal">Unique Visitors</h5>
                      <h2 class="mb-4 text-dark font-weight-bold">756,00</h2>
                      <radial-progress-bar class="ml-auto mr-auto" :diameter="125"
                        :completed-steps="60"
                        :total-steps="100"
                        innerStrokeColor="#eee"
                        startColor = "#b4ec51"
                        stopColor="#429321"
                        :strokeWidth="7"
                        >
                        <i class="mdi mdi-account-circle icon-md absolute-center text-dark"></i>
                      </radial-progress-bar>
                      <p class="mt-4 mb-0">Increased since yesterday</p>
                      <h3 class="mb-0 font-weight-bold mt-2 text-dark">50%</h3>
                    </div>
                  </div>
                </div>
                <div class="col-xl-3  col-lg-6 col-sm-6 grid-margin stretch-card">
                  <div class="card">
                    <div class="card-body text-center">
                      <h5 class="mb-2 text-dark font-weight-normal">Impressions</h5>
                      <h2 class="mb-4 text-dark font-weight-bold">100,38</h2>
                        <radial-progress-bar class="ml-auto mr-auto" :diameter="125"
                        :completed-steps="90"
                        :total-steps="100"
                        innerStrokeColor="#eee"
                        startColor = "#fad961"
                        stopColor="#f76b1c"
                        :strokeWidth="7"
                        >
                        <i class="mdi mdi-eye icon-md absolute-center text-dark"></i>
                      </radial-progress-bar>
                      <p class="mt-4 mb-0">Increased since yesterday</p>
                      <h3 class="mb-0 font-weight-bold mt-2 text-dark">35%</h3>
                    </div>
                  </div>
                </div>
                <div class="col-xl-3 col-lg-6 col-sm-6 grid-margin stretch-card">
                  <div class="card">
                    <div class="card-body text-center">
                      <h5 class="mb-2 text-dark font-weight-normal">Followers</h5>
                      <h2 class="mb-4 text-dark font-weight-bold">4250k</h2>
                        <radial-progress-bar class="ml-auto mr-auto" :diameter="125"
                        :completed-steps="45"
                        :total-steps="100"
                        innerStrokeColor="#eee"
                        startColor = "#f5515f"
                        stopColor="#9f041b"
                        :strokeWidth="7"
                        >
                        <i class="mdi mdi-cube icon-md absolute-center text-dark"></i>
                      </radial-progress-bar>
                      <p class="mt-4 mb-0">Decreased since yesterday</p>
                      <h3 class="mb-0 font-weight-bold mt-2 text-dark">25%</h3>
                    </div>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-12 grid-margin">
                  <div class="card">
                    <div class="card-body">
                      <div class="row">
                        <div class="col-sm-12">
                          <div class="d-flex justify-content-between align-items-center mb-4">
                            <h4 class="card-title mb-0">Recent Activity</h4>
                            <b-dropdown id="ddown35" text="Dropdown" variant="white" class="bg-white ml-0 ml-md-4 mt-2 mt-lg-0 dotted-btn-transparent">
                              <template slot="button-content">
                                <span class="py-3" id="calendarDrop" href="javascript:void(0);" data-toggle="dropdown" aria-expanded="false">
                                  <i class="mdi mdi-dots-vertical"></i>
                                </span>
                              </template>
                              <b-dropdown-item>Settings</b-dropdown-item>
                              <b-dropdown-item>Action</b-dropdown-item>
                              <b-dropdown-item>Another action</b-dropdown-item>
                              <b-dropdown-divider></b-dropdown-divider>
                              <b-dropdown-item>Something else here...</b-dropdown-item>
                              <b-dropdown-item disabled>Disabled action</b-dropdown-item>
                            </b-dropdown>
                          </div>
                        </div>
                        <div class="col-lg-3 col-sm-4 grid-margin  grid-margin-lg-0">
                          <div class="wrapper pb-5 border-bottom">
                            <div class="text-wrapper d-flex align-items-center justify-content-between mb-2">
                              <p class="mb-0 text-dark">Total Profit</p>
                              <span class="text-success"><i class="mdi mdi-arrow-up"></i>2.95%</span>
                            </div>
                            <h3 class="mb-0 text-dark font-weight-bold">$ 92556</h3>
                            <totalProfit :height="200"></totalProfit>
                          </div>
                          <div class="wrapper pt-5">
                            <div class="text-wrapper d-flex align-items-center justify-content-between mb-2">
                              <p class="mb-0 text-dark">Expenses</p>
                              <span class="text-success"><i class="mdi mdi-arrow-up"></i>52.95%</span>
                            </div>
                            <h3 class="mb-4 text-dark font-weight-bold">$ 59565</h3>
                            <totalExpence :height="200"></totalExpence>
                          </div>
                        </div>
                        <div class="col-lg-9 col-sm-8 grid-margin  grid-margin-lg-0">
                          <div class="pl-0 pl-lg-4 ">
                            <div class="d-xl-flex justify-content-between align-items-center mb-2">
                              <div class="d-lg-flex align-items-center mb-lg-2 mb-xl-0">
                                <h3 class="text-dark font-weight-bold mr-2 mb-0">Devices sales</h3>
                                <h5 class="mb-0">( growth 62% )</h5>
                              </div>
                              <div class="d-lg-flex">
                                <p class="mr-2 mb-0">Timezone:</p>
                                <p class="text-dark font-weight-bold mb-0">GMT-0400 Eastern Delight Time</p>
                              </div>
                            </div>
                            <div class="graph-custom-legend clearfix" id="device-sales-legend"></div>
                            <div class="rounded-legend legend-horizontal legend-top-right float-right">
                              <ul>
                                <li class="text-dark">
                                  <div class="d-flex align-items-center">
                                    <span class="legend-dots bg-info"></span><span class="legend-label text-dark">Demand</span>
                                  </div>
                                </li> 
                                <li class="text-dark">
                                  <div class="d-flex align-items-center">
                                    <span class="legend-dots bg-danger"></span><span class="legend-label text-dark">Supply</span>
                                  </div>
                                </li> 
                              </ul>
                            </div>
                            <deviceSales :height="214"></deviceSales>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="row">  
                <div class="ol-xl-4 col-sm-5 grid-margin stretch-card">
                  <div class="card card-danger-gradient">
                    <div class="card-body mb-4">
                      <h4 class="card-title text-white">Account Retention</h4>
                      <accountRetension :height="220"></accountRetension>
                    </div>
                    <div class="card-body bg-white pt-4">
                      <div class="row pt-4">
                        <div class="col-sm-6">
                          <div class="text-center border-right border-md-0">
                            <h4>Conversion</h4>
                            <h1 class="text-dark font-weight-bold mb-md-3">$306</h1>
                          </div>
                        </div>
                        <div class="col-sm-6">
                          <div class="text-center">
                            <h4>Cancellation</h4>
                            <h1 class="text-dark font-weight-bold">$1,520</h1>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="ol-xl-8 col-sm-7  grid-margin stretch-card">
                  <div class="card">
                    <div class="card-body">
                      <div class="d-xl-flex justify-content-between mb-2">
                        <h4 class="card-title">Page views analytics</h4>
                        <div class="rounded-legend legend-horizontal legend-top-right float-right">
                          <ul>
                            <li class="text-dark">
                              <div class="d-flex align-items-center">
                                <span class="legend-dots bg-success"></span><span class="legend-label text-dark">This week</span>
                              </div>
                            </li> 
                            <li class="text-dark">
                              <div class="d-flex align-items-center">
                                <span class="legend-dots bg-primary"></span><span class="legend-label text-dark">Current week</span>
                              </div>
                            </li> 
                          </ul>
                        </div>
                      </div>
                      <pageViewAnalytics :height="250"></pageViewAnalytics>
                    </div>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-sm-4 grid-margin grid-margin-lg-0 stretch-card">
                  <div class="card">
                    <div class="card-body recent-activity">
                      <h4 class="card-title">Recent Activity</h4>
                      <div class="d-flex mb-3">
                        <div>
                          <div class="activity-info bg-danger"> I </div>
                        </div>
                        <div class="activity-details">
                          <h4 class="text-dark font-weight-normal">Iva Barber</h4>
                          <p class="mb-0">added new task on trello</p>
                          <p class="text-small mb-0">05:58AM</p>
                        </div>
                      </div>
                      <div class="d-flex mb-3">
                        <div class="activity-info bg-warning"> D </div>
                        <div class="activity-details">
                          <h4 class="text-dark font-weight-normal">Dorothy Romero</h4>
                          <p class="mb-0">added new task on trello</p>
                          <p class="text-small mb-0">02:50PM</p>
                        </div>
                      </div>
                      <div class="d-flex mb-3">
                        <div class="activity-info bg-success"> R </div>
                        <div class="activity-details">
                          <h4 class="text-dark font-weight-normal">Ricardo Hawkins</h4>
                          <p class="mb-0">added new task on trello</p>
                          <p class="text-small mb-0">05:22AM</p>
                        </div>
                      </div>
                      <div class="d-flex">
                        <div class="activity-info hide-border bg-info"> N </div>
                        <div class="activity-details">
                          <h4 class="text-dark font-weight-normal">Noah Montgomery</h4>
                          <p class="mb-0">added new task on trello</p>
                          <p class="text-small mb-0">08:19PM</p>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="col-sm-4 grid-margin grid-margin-lg-0 stretch-card">
                  <div class="card">
                    <div class="card-body">
                      <h4 class="card-title">My Balance</h4>
                      <div class="d-lg-flex justify-content-between align-items-center">
                        <h1 class="text-dark mb-0">$3258</h1>
                        <p class="text-success mb-0 font-weight-medium">+30.56% ($121)</p>
                      </div>
                      <p class="mb-5 pb-1">Deposit: <span class="font-weight-bold">$5430</span></p>
                      <myBalance :height="200"></myBalance>
                      <div class="border p-3 mt-2">
                        <div class="row">
                          <div class="col-sm-6 mb-4 mb-lg-0">
                            <div class="d-lg-flex justify-content-between align-items-center mb-1">
                              <div class="text-small text-dark">Available :</div>
                              <span class="font-weight-bold text-dark text-small ">30.56%</span>
                            </div>
                              <b-progress :value="25" variant="success"></b-progress>
                          </div>
                          <div class="col-sm-6">
                            <div class="d-lg-flex justify-content-between align-items-center mb-1">
                              <div class="text-small text-dark">Pending :</div>
                              <span class="font-weight-bold text-small text-dark">69.44%</span>
                            </div>
                              <b-progress :value="70" variant="info"></b-progress>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="col-sm-4 grid-margin grid-margin-lg-0 stretch-card">
                  <div class="card">
                    <div class="card-body">
                      <div class="dotted-border p-3 mb-3">
                        <div class="row">
                          <div class="col-sm-12">
                            <h4 class="card-title mb-1">Sales Prediction</h4>
                          </div>
                          <div class="col-sm-6">
                            <salesPredictionLeft :height="220"></salesPredictionLeft>
                            <h3 class="font-weight-bold mt-3 text-dark">$3258</h3>
                            <p class="text-muted mb-0">350-985 sales</p>
                          </div>
                          <div class="col-sm-6">
                            <salesPredictionRight :height="220"></salesPredictionRight>
                            <h3 class="font-weight-bold mt-3 text-dark">$3258</h3>
                            <p class="text-muted mb-0">350-985 sales</p>
                          </div>
                        </div>
                      </div>
                      <div class="dotted-border p-3">
                        <div class="row">
                          <div class="col-sm-12">
                            <h4 class="card-title mb-1">Stock History</h4>
                          </div>
                          <div class="col-sm-6">
                            <stockHistoryLeft :height="220"></stockHistoryLeft>
                            <h3 class="font-weight-bold mt-3 text-dark">$3258</h3>
                            <p class="mb-0 text-muted">350-985 sales</p>
                          </div>
                          <div class="col-sm-6">
                            <stockHistoryRight :height="220"></stockHistoryRight>
                            <h3 class="font-weight-bold text-dark  mt-3">$3258</h3>
                            <p class="mb-0 text-muted">350-985 sales</p>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </b-tab>
          <b-tab title="Performance" disabled>
            <div>3</div>
          </b-tab>
          <b-tab title="Conversion" disabled>
            <div>4</div>
          </b-tab>
        </b-tabs>
      </div>
    </div>
  </section>
</template>

<script>

import RadialProgressBar from 'vue-radial-progress'
import totalProfit from '../../components/charts/dashboard/totalProfit'
import totalExpence from '../../components/charts/dashboard/totalExpence'
import deviceSales from '../../components/charts/dashboard/deviceSales'
import accountRetension from '../../components/charts/dashboard/accountRetension'
import pageViewAnalytics from '../../components/charts/dashboard/pageViewAnalytics'
import myBalance from '../../components/charts/dashboard/myBalance'
import salesPredictionLeft from '../../components/charts/dashboard/salesPredictionLeft'
import salesPredictionRight from '../../components/charts/dashboard/salesPredictionRight'
import stockHistoryLeft from '../../components/charts/dashboard/stockHistoryLeft'
import stockHistoryRight from '../../components/charts/dashboard/stockHistoryRight'

export default {
  name: 'dashboard',
  components: {
    RadialProgressBar,
    totalProfit,
    totalExpence,
    deviceSales,
    accountRetension,
    pageViewAnalytics,
    myBalance,
    salesPredictionLeft,
    salesPredictionRight,
    stockHistoryLeft,
    stockHistoryRight
  },
  data() {
    return {
    };
  },
  methods: {
    toggleProBanner: () => {
      document.querySelector('body').classList.toggle('pro-banner-collapse');
    }
  }
}
</script>

<style scoped>

</style>