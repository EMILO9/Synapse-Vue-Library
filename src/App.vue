<template>
  <synapseApp>
    <synapseHeader :mobileMenuOpen="mobileMenuOpen">
      <template v-slot:logo><synapseMenu><synapseLogo>YOUR LOGO</synapseLogo><synapseSearch/></synapseMenu></template>
      <template v-slot:menu><synapseMenu>
        <synapseButton
        @click.native="setActive(n)"
        v-for="(n, index) in buttons"
        :key="n+index"
        :button="n"/>
        </synapseMenu>
      </template>
    </synapseHeader>
    <synapseContent v-if="page===1">
      <synapseRow>
        <synapseColumn v-for="n in 1002" :key="n">col{{n}} Lorem ipsum dolor, sit amet consectetur adipisicing elit. Soluta consequatur saepe ipsa atque aperiam quae impedit neque animi excepturi quas.</synapseColumn>
      </synapseRow>
    </synapseContent>
    <synapseFooter>© Copyright</synapseFooter>
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
import synapseSearch from './components/synapseSearch'
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
    synapseMobileMenu,
    synapseSearch
  },
  data () {
    return {
      buttons: [
        {Name: 'Page1', isActive: true, fontClass: 'fas fa-sad-tear'},
        {Name: 'Page2', isActive: false, fontClass: 'fas fa-meh'},
        {Name: 'Page3', isActive: false, fontClass: 'fas fa-smile-beam'},
        {Name: 'Page4', isActive: false, fontClass: 'fas fa-sad-cry'},
        {Name: 'Page5', isActive: false, fontClass: 'fas fa-meh-rolling-eyes'}
      ],
      mobileMenuOpen: false,
      page: 1,
      search: ''
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
    eventBus.$on('setSearch', data => { this.search = data })
  }
}
</script>
