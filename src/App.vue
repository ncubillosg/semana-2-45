<template>
  <div id="app">
    <Header />
    <main>
      <Team />
    </main>
    <Footer />
  </div>
</template>

<script>
import Team from './components/Team';
import Header from './components/Header';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Team,
    Header,
    Footer
  }
}
</script>

