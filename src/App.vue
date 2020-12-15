<template>
  <div id="app">

    <!---News--->
    <div >
      <p class="d-block p-2 bg-dark text-white justify-content-center text-center">Noticias</p>
      <div clas="d-flex container-fluid flex-wrap">
        
            <news></news>           
        
      </div>
    </div>   
    
  </div>
</template>

<script>
import News from './components/News.vue'

export default {
  name: 'App',
  components: { 
    News 
    },
}
</script>

