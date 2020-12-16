<template>
  <div id="app">
    <Header />
    <main>
      <Services />
      <News />
      <Team />
    </main>
    <Footer />
  </div>
</template>

<script>
import Team from './components/Team';
import Header from './components/Header';
import Footer from './components/Footer';
import News from './components/News';
import Services from './components/Services';

export default {
  name: 'App',
  components: {
    Team,
    Header,
    Footer,
    News,
    Services
  }
}
</script>

