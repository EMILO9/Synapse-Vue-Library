<template>
  <synapseApp>
    <synapseHeader :mobileMenuOpen="mobileMenuOpen">
      <template v-slot:logo><synapseMenu><synapseLogo>YOUR LOGO</synapseLogo></synapseMenu></template>
      <template v-slot:menu><synapseMenu>
        <synapseButton
        @click.native="setActive(n)"
        v-for="(n, index) in buttons"
        :key="n+index"
        :button="n"/>
        </synapseMenu>
      </template>
    </synapseHeader>
    <synapseContent>
      <synapseRow>
        <synapseColumn v-for="n in 10000" :key="n">Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, natus ratione aliquid iste eos corporis, odit repellat sequi non, dicta minima atque est earum. Cupiditate maiores sunt a magni numquam!</synapseColumn>
      </synapseRow>
    </synapseContent>
    <synapseFooter>Copyright</synapseFooter>
    <synapseMobileMenu :mobileMenuOpen="mobileMenuOpen" :buttons="buttons"/>
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
import synapseMobileMenu from './components/synapseMobileMenu'
import { eventBus } from './main'
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
    synapseLogo,
    synapseMobileMenu
  },
  data () {
    return {
      buttons: [
        {Name: 'Page1', isActive: true},
        {Name: 'Page2', isActive: false},
        {Name: 'Page3', isActive: false},
        {Name: 'Page4', isActive: false},
        {Name: 'Page5', isActive: false}
      ],
      mobileMenuOpen: false
    }
  },
  methods: {
    setActive (n) {
      for (let button of this.buttons) { button.isActive = false }
      n.isActive = true
      this.mobileMenuOpen = false
    }
  },
  created () {
    eventBus.$on('setMenu', () => { this.mobileMenuOpen = true })
    eventBus.$on('selectMenu', (data) => { this.setActive(data) })
    eventBus.$on('closeMenu', data => { this.mobileMenuOpen = data })
  }
}
</script>
