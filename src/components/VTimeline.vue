<template>
  <ul>
    <step v-for="(stepData, index) in data" :key="index" :step-data="stepData" />
  </ul>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import { StepInt, TimelineOptionsInt } from '@/interfaces/'
import Step from './Step'

@Component({
  name: 'VTimeline',
  components: { Step }
})
export default class VTimeline extends Vue {
  
  @Prop({required: true})
  data: StepInt[]
  
  @Prop({
    default: () => {
      return {
        dir: 'horizontal',
        allowWrap: false,
        wrapSnake: false,
      }
    }
  })
  options: TimelineOptionsInt
}
</script>

<style lang="scss" scoped>

</style>
