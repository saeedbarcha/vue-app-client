

<template>
  <div id="app">
    <AppHeader />
    <section class="content">
      <AppSidebar />
      <DataTable />
    </section>

  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue';
import AppSidebar from '@/components/AppSidebar.vue';
import DataTable from '@/components/DataTable.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppSidebar,
    DataTable
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
}
#app {
  height: 100%;
  width: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding:0rem;
  margin: 0rem;
  display: flex;
  flex-direction: column;
}

.content {
  display: flex;
  padding: 1% 2%;
  height: 82vh;
  flex-direction: row;
  background-color: rgb(255, 255, 255);
}
</style>
