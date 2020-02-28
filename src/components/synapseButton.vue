<template>
  <button class="synapse-button" :class="{'synapse-button-active': button.isActive}">{{button.Name}}</button>
</template>

<script>
export default {
  name: 'synapseButton',
  props: ['button'],
  data () {
    return {}
  }
}
</script>
