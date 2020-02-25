<template>
  <div
  class="synapse-app"
  id="app"
  :style="{ 'background-color': backgroundColor, 'grid-template-rows': rows }"
  >
  <slot/>
  </div>
</template>

<script>
export default {
  name: 'synapseApp',
  props: ['backgroundColor', 'rows'],
  data () {
    return {}
  }
}
</script>
