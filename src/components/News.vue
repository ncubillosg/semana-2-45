<template>
    <div>
        <div class="container">
            <h2>News</h2>
            <hr>
            <div class="row">
                <div class="newsCard mb-4 col-lg-6 col-xs-12" v-for="(item, index) of this.info" :key="index">
                    <div class="col-12">
                        <div class="d-flex align-items-center justify-content-between align-content-center">
                            <img src="https://i.picasion.com/pic90/96f94ea318bfd9ede1d311621d6696f2.gif" height="200" class="mr-2" alt="coffeeNews" >
                            <div class="body">
                                <p>{{ item.title }}</p>
                                <p class="text-justify">{{ item.description.slice(0,200) }}...</p>
                                <span>{{ item.author }}</span>
                            </div>
                        </div>
                        <a :href="item.url" target="_blank" class="infobtn">
                            <button type="button" class="btn btn-outline-info" >info</button>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
 </template>

<script>
    import axios from "axios";
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
    .newsCard {
        position: relative;
        padding: 0;
    }

    .infobtn {
        position: absolute;
        right: 0;
        bottom: 0;
    }

    .newsCard>.d-flex {
        height: 100%;
    }

</style>