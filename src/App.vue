<template>
  <div id="app">
    <v-timeline :data="timelineData" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import VTimeline from './components/VTimeline'
import { StepInt } from '@/interfaces/'

import moment from 'moment'

@Component({
  components: { VTimeline }
})
export default class App extends Vue {
  
  timeLineDataLength = 5
  timelineData: StepInt[] = []

  mounted () {
    this.createData()
  }

  createData () {
    this.timelineData = [...Array(this.timeLineDataLength)].fill(null).map((x, i) => {
      return {
        date: moment().subtract(i, 'days').format(),
        title: `Step ${i}`,
        description: `This is a description for ste ${i}`
      }
    })
  }

}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
