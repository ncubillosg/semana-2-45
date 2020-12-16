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

export default {
    name: "Team",
    components: {
        teamcard
    },
    data() {
        return {
            members
        }
    }
}
</script>
<style>

</style>