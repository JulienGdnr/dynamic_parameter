<template>
  <div id="app">
    <button @click.prevent="getData">Reset last month</button>
  </div>
</template>

<script>
require('./extension.js');
export default {
  name: 'home',
  data(){
    return {
      dashboard : null,
      year : 0,
      month : 0,
      months : ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"]
    }
  },
  methods : {
    getData(){
      this.dashboard.findParameterAsync("Month")
      .then(data=>{
          data.changeValueAsync(this.months[this.month])
      })
      this.dashboard.findParameterAsync("Year")
      .then(data=>{
        data.changeValueAsync(this.year)
      })
    }
  },
  mounted(){
    const d = new Date()
    this.year = d.getYear() + 1900
    this.month = d.getMonth()
    if(this.month == 0){
      this.month = 11
      this.year = this.year - 1
    } else {
      this.month = this.month - 1
    }
    tableau.extensions.initializeAsync()
    .then(() => {
      this.dashboard = tableau.extensions.dashboardContent.dashboard
      this.getData()
    })
 }
}
</script>
