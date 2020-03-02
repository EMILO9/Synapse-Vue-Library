<template>
  <div
  class="synapse-header"
  >
    <slot name="logo"/>
    <slot name="menu" v-if="width >= 1200"/>
      <synapseMenu v-else>
        <button @click="openMobileMenu" class="synapse-button" style="font-size: 30px;"><i class="fas fa-bars"></i></button>
      </synapseMenu>
  </div>
</template>

<script>
import synapseMenu from './synapseMenu'
import { eventBus } from '../main'
export default {
  name: 'synapseHeader',
  props: ['mobileMenuOpen'],
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
    handleResize () { this.width = window.innerWidth },
    openMobileMenu () {
      eventBus.$emit('setMenu')
    }
  },
  watch: {
    width: function () { if (this.width > 1200) eventBus.$emit('closeMenu') }
  }
}
</script>
