<template>
  <synapseApp>
    <synapseHeader>
      <template v-slot:logo><synapseMenu><span style="margin-left:10px; font-size: 40px;">LOGO</span></synapseMenu></template>
      <template v-slot:menu><synapseMenu>
        <button class="synapse-button" v-for="item in 5" :key="item">Button{{item}}</button>
        </synapseMenu></template>
    </synapseHeader>
    <synapseContent>
      <synapseRow>
        <synapseColumn v-for="n in 3" :key="n">Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, natus ratione aliquid iste eos corporis, odit repellat sequi non, dicta minima atque est earum. Cupiditate maiores sunt a magni numquam!</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 20" :key="n">Lorem ipsum dolor sit amet.</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 300" :key="n">Lorem ipsum dolor sit amet.</synapseColumn>
      </synapseRow>
    </synapseContent>
    <synapseFooter></synapseFooter>
  </synapseApp>
  <!-- Next: add props to each component -->
</template>

<script>
import synapseApp from './components/synapseApp'
import synapseHeader from './components/synapseHeader'
import synapseContent from './components/synapseContent'
import synapseFooter from './components/synapseFooter'
import synapseRow from './components/synapseRow'
import synapseColumn from './components/synapseColumn'
import synapseMenu from './components/synapseMenu'
export default {
  name: 'App',
  components: {
    synapseApp,
    synapseHeader,
    synapseContent,
    synapseFooter,
    synapseRow,
    synapseColumn,
    synapseMenu
  }
}
</script>
