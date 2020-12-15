<template>
<div class="row mt-md-5 mt-sm-5 mt-xs-5" >
    <div class="col-lg-6 col-xs-12" v-for="(item,index) of this.info" :key="index">
        <div clas="container-fluid" >
        <div class="d-flex justify-content-center align-items-center">
            <div class="p-3">
                <img src="https://i.picasion.com/pic90/96f94ea318bfd9ede1d311621d6696f2.gif" width="200" height="200" border="0" alt="coffeeNews" >
            </div>
            <div class="p-2">
               <p>{{ item.title }}</p>
               <p>{{ item.description.slice(0,250) }}</p>
               <p>{{ item.author }}</p>
            </div>
        </div>
        <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
            <button type="button" class="btn btn-outline-info" >
               <a :href="item.url" >info</a>
            </button>
        </div>
        </div>
    </div>
</div>
    
</template>

<script>
    import axios from "axios"
    export default {
        name: "News",
        data(){
            return{
               info : null
               }
        },
        created() {
        axios
          //.get('http://newsapi.org/v2/everything?q=cafe&apiKey=2022a7cec6584983961e4a5b0be521e5')
          .get('http://api.mediastack.com/v1/news?access_key=2b5c445f132a804c5a6b126ea5828018&keywords=coffee&countries=us,co&sources=business&limit=10')
          .then(response => (this.info = response.data.data.slice(3,7)))
          .catch(error => console.log(error))
        }
    }
</script>

<style scoped>


</style>