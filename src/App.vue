<template>
  <div>
    <nav>
      <h2>Vue Collapsible Table</h2>
    </nav>

    <main>
      <HelloWorld/>
    </main>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
nav {
  width: 100%;
  height: 80px;
  background: #273052;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #ffffff;
  text-transform: uppercase;
}
</style>