<template>
  <component :is="`${layout}-layout`" />
</template>

<script>
import { computed } from 'vue'
import { useRoute } from 'vue-router'
import { useStore } from 'vuex'
import MainLayout from './layout/MainLayout'
import AuthLayout from './layout/AuthLayout'
import EmptyLayout from './layout/EmptyLayout'
export  default  {
  setup() {
    const route = useRoute()
    const store = useStore()

    const fetchProducts = () => store.dispatch('product/fetchProducts')
    const fetchCategories = () => store.dispatch('category/fetchCategories')

    return {
      layout: computed(() => route.meta?.layout),
      fetchProducts,
      fetchCategories
    }
  },
  components: {
    MainLayout,
    AuthLayout,
    EmptyLayout
  },
  created() {
    this.fetchCategories()
    this.fetchProducts()
  }
}
</script>
<style lang="scss">
@import '../src/assets/scss/style.scss';
</style>
