<template>

        <header class="bg-primary-1 py-3">
                <div class="max-w-6xl flex justify-between px-4 mx-auto items-center text-white-ui">
            <div class="flex items-center gap-x-4">
                <font-awesome-icon class="text-secondary-2 text-2xl mr-5 cursor-pointer" :icon="myIcon" />
                <font-awesome-icon class="text-secondary-2 text-2xl" :icon="legalIcon" />
                <p class="text-lg">Robar y Servir</p>
            </div>
            <div class="flex items-center gap-x-4">
                <p class="text-lg">Bienvenido Profesor</p>
            
                  <nuxt-link to="/" class="flex items-center gap-x-2">
                  <font-awesome-icon class="text-secondary-2 text-2xl cursor-pointer ml-6" :icon="exitIcon" />
                  <p>Salir</p>
                  </nuxt-link>
          
            </div>
                </div>
        </header>

</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faBars, faBalanceScale, faDoorOpen } from '@fortawesome/free-solid-svg-icons'

export default {
  name: 'MyComponent',

  data () {
    return {
      myIcon: faBars,
      legalIcon: faBalanceScale,
      exitIcon: faDoorOpen
    }
  },

  components: {
    FontAwesomeIcon
  }
}
</script>