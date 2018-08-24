<template>
  <li>
    <p>{{stepData.date}}</p>
    <p>{{stepData.title}}</p>
    <p>{{stepData.description}}</p>
  </li>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import { StepInt } from '@/interfaces/'

@Component({
  name: 'Step'
})
export default class VTimeline extends Vue {
  @Prop({ required: true })
  stepData: StepInt
}
</script>

<style lang="scss" scoped>

</style>
