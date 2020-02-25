<template>
  <div
  class="synapse-content"
  :style="{ 'background-color': backgroundColor, 'padding': padding }"
  >
  <slot/>
  </div>
</template>

<script>
export default {
  name: 'synapseContent',
  props: ['backgroundColor', 'padding'],
  data () {
    return {}
  }
}
</script>
