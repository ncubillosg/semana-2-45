<template>
    <div class="col-md-6 col-lg-3">
        <div class="col-12 member">
            <img :src="member.image" alt="imagen-integrante">
            <h3 class="text-center">{{member.nombre}}</h3>
            <h4 class="text-center">{{member.rol}}</h4>
            <p class="text-center">{{member.descripcion}}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "teamcard",
        props: ['member']
    }
</script>

<style scoped>

</style>
