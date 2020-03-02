 <template>
<div class="synapse-mobile-menu" v-if="mobileMenuOpen">
    <div class="synapse-close-button"><i class="fas fa-times" @click="closeMenu"></i></div>
    <div class="synapse-all-menu-options">
        <div
        @click="run(b)"
        :class="{'synapse-mobile-menu-item-active': b.isActive}"
         class="synapse-mobile-menu-item"
         v-for="(b, index) in buttons" :key="b+index">{{b.Name}}</div>
    </div>
</div>
</template>

<script>
import { eventBus } from '../main'
export default {
  name: 'synapseMobileMenu',
  props: ['mobileMenuOpen', 'buttons'],
  data () {
    return {}
  },
  methods: {
    run (b) {
      eventBus.$emit('selectMenu', b)
    },
    closeMenu () {
      eventBus.$emit('closeMenu', false)
    }
  }
}
</script>
