<template>
  <div
  class="synapse-header"
  :style="{ 'background-color': backgroundColor }"
  >
  </div>
</template>

<script>
export default {
  name: 'synapseHeader',
  props: ['backgroundColor'],
  data () {
    return {}
  }
}
</script>
