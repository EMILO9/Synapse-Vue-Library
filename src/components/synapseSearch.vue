<template>
<input @input="setSearch($event)" class="synapse-search" type="search" placeholder="search">
</template>

<script>
import { eventBus } from '../main'
export default {
  name: 'synapseSearch',
  data () {
    return {}
  },
  methods: {
    setSearch (e) { eventBus.$emit('setSearch', e.target.value) }
  }
}
</script>
