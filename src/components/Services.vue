<template>
    <div id="services">
    <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
      <ol class="carousel-indicators">
        <li data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active"></li>
        <li data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1"></li>
        <li data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2"></li>
      </ol>
      <div class="carousel-inner slider-size">
        <div class="carousel-item active">
            
          <img src="https://media.istockphoto.com/photos/coffee-beans-and-cream-picture-id862471728" width="86%" height="700" class="d-block sliders-images" alt="Calidad del Grano" >
          <div class="carousel-caption d-none d-md-block">
            <h3>La calidad del Café</h3>
            <p class="paragraph-sliders-text">En esta sección descubriras la ciencia y dedicación en la preparación del grano.</p>
          </div>
        </div>
        <div class="carousel-item">
          <img src="https://media.istockphoto.com/photos/traditional-coffee-cup-with-heartshaped-steam-on-rustic-wood-picture-id517518956" width="86%" height="700" class="d-block sliders-images" alt="Consumir Producto">
          <div class="carousel-caption d-none d-md-block">
            <h3>Consumir nuestros productos</h3>
            <p class="paragraph-sliders-text">Los diferentes aromas y texturas están presentes en nuestra marca, así podrás conocer y elegir tu preferencia.</p>
          </div>
        </div>
        <div class="carousel-item">
          <img src="https://st2.depositphotos.com/6672578/9897/i/950/depositphotos_98977056-stock-photo-coffee-shop-with-customers-sitting.jpg" width="86%" height="700" class="d-block sliders-images" alt="Franquicia de Tiendas">
          <div class="carousel-caption d-none d-md-block">
            <h3>Nuestra Franquicia</h3>
            <p class="paragraph-sliders-text">Ser la marca más reconocida a nivel mundial es un trabajo de equipo, aquí podrás conocernos.</p>
          </div>
        </div>
      </div>
      <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
    name: "Services"
}
</script>

<style>
/* Estilo para los servicios */
.sliders-images {
    display: block;
    margin-left: auto;
    margin-right: auto;
    border:none;
}

.slider-size{
    width: 600;
    height: 400;
}

.paragraph-sliders-text{
    font-size: 20px;
    font-style: italic;
}
</style>