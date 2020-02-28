<template>
  <synapseApp>
    <synapseHeader>
      <template v-slot:logo><synapseMenu><synapseLogo>YOUR LOGO</synapseLogo></synapseMenu></template>
      <template v-slot:menu><synapseMenu>
        <synapseButton @click.native="setActive(n)" v-for="n in buttons" :key="n" :button="n"/>
        </synapseMenu></template>
    </synapseHeader>
    <synapseContent>
      <synapseRow>
        <synapseColumn v-for="n in 3" :key="n">Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, natus ratione aliquid iste eos corporis, odit repellat sequi non, dicta minima atque est earum. Cupiditate maiores sunt a magni numquam!</synapseColumn>
      </synapseRow>
      <synapseRow>
        <synapseColumn v-for="n in 30" :key="n">Lorem ipsum dolor sit amet.</synapseColumn>
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
import synapseButton from './components/synapseButton'
import synapseLogo from './components/synapseLogo'
export default {
  name: 'App',
  components: {
    synapseApp,
    synapseHeader,
    synapseContent,
    synapseFooter,
    synapseRow,
    synapseColumn,
    synapseMenu,
    synapseButton,
    synapseLogo
  },
  data () {
    return {
      buttons: [
        {Name: 'Button1', isActive: true},
        {Name: 'Button2', isActive: false},
        {Name: 'Button3', isActive: false},
        {Name: 'Button4', isActive: false},
        {Name: 'Button5', isActive: false}
      ]
    }
  },
  methods: {
    setActive (n) {
      for (let button of this.buttons) { button.isActive = false }
      n.isActive = true
    }
  }
}
</script>
