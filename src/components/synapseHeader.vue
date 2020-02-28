<template>
  <div
  class="synapse-header"
  >
    <slot name="logo"/>
    <slot name="menu" v-if="width > 1200"/>
      <synapseMenu v-else>
        <button class="synapse-button" style="font-size: 40px;"><i class="fas fa-bars"></i></button>
      </synapseMenu>
  </div>
</template>

<script>
import synapseMenu from './synapseMenu'
export default {
  name: 'synapseHeader',
  components: {
    synapseMenu
  },
  data () {
    return {
      width: 0
    }
  },
  created () {
    window.addEventListener('resize', this.handleResize)
    this.handleResize()
  },
  methods: {
    handleResize () { this.width = window.innerWidth; console.log(this.width) }
  }
}
</script>
