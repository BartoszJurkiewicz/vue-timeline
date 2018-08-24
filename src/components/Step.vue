<template>
  <li>
    <p>{{stepData.date}}</p>
    <p>{{stepData.title}}</p>
    <p>{{stepData.description}}</p>
  </li>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { StepInt } from '@/interfaces/'

@Component({
  props: {
    stepData: Object
  }
})
export default class VTimeline extends Vue {
  stepData: StepInt
}
</script>

<style lang="scss" scoped>

</style>
