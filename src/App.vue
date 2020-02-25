<template>
  <synapseApp backgroundColor="default" rows="default">
    <synapseHeader backgroundColor="default"/>
    <synapseContent backgroundColor="default" padding="default">
      <!-- Place you content here! -->
    </synapseContent>
    <synapseFooter backgroundColor="default"/>
  </synapseApp>
</template>

<script>
import synapseApp from './components/synapseApp'
import synapseHeader from './components/synapseHeader'
import synapseContent from './components/synapseContent'
import synapseFooter from './components/synapseFooter'

export default {
  name: 'App',
  components: {
    synapseApp,
    synapseHeader,
    synapseContent,
    synapseFooter
  }
}
</script>
