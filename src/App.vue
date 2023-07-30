<script setup>
  import { ref } from 'vue'
  import { useElementVisibility  } from '@vueuse/core'
  import HelloWorld from './components/HelloWorld.vue'

  const templateRef = ref(null)
  const isElementVisible = useElementVisibility(templateRef)
</script>

<template>
  <HelloWorld :msg="'this is a message'"/>
  <main
    ref="templateRef"
    class="p-3 bg-slate-500" >
    Testing 
  </main>

  <div class="h-[110vh]"></div>

  <section class="fixed bottom-0 right-0">is visible: {{ isElementVisible }}</section>

</template>
