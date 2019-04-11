<template>
      <div class="card">
            <div class="card-content">
                  <div class="row valign-wrapper">
                          <grid-vue tamanho="1">
                            <img :src="perfil" :alt="nome" class="circle responsive-img"> <!-- notice the "circle" class -->
                          </grid-vue>

                          <grid-vue tamanho="11">
                              <span class="black-text">
                                <strong>{{nome}}</strong> - <small>{{data}}</small>
                              </span>
                          </grid-vue>
                  </div>

                  <slot />

            </div>
            <div class="card-action">
                  <a href="#">This is a link</a>
                  <a href="#">This is a link</a>
            </div>
      </div>
</template>

<script>
import GridVue from '@/components/layouts/GridVue'
export default {
  name: 'CardConteudoVue.vue',
  props:['perfil','nome','data'],
  data () {
    return {

    }
  },
  components:{
  GridVue
   }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
