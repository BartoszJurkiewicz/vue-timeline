<template>
  <ul>
    <step v-for="(stepData, index) in data" :key="index" :step-data="stepData" />
  </ul>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { StepInt } from '@/interfaces/'
import Step from './Step'

@Component({
  props: {
    data: Array
  },
  components: { Step }
})
export default class VTimeline extends Vue {
  data: StepInt[]
}
</script>

<style lang="scss" scoped>

</style>
