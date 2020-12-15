<template>
  <div class="container" id="team">
        <h2>Nuestro equipo</h2>
        <hr>
        <div class="row" v-if="members!=[]">
            <teamcard v-for="item in members" v-bind:member="item" v-bind:key="item.codigo"></teamcard>
        </div>
    </div>
</template>

<script>
import teamcard from './TeamCard.vue';
import members from '../team.json';

/* const call = async query => {
    const response = await fetch(query);
    const data = await response.json();

    console.log(data);
    return data;
}; */

export default {
    name: "Team",
    components: {
        teamcard
    },
    data() {
        return {
            members
        }
    },
    /* created() {
        call("../team.json")
            .then(data => {
                console.log(data);
                this.members = data;
            })
            .catch(err => console.error(err));
    } */
}
</script>
<style>

</style>