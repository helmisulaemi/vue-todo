<template>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/profile">Profile</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/> -->
  <div class="todoApp">
    <div class="container mt-5">
      <div class="row header mb-5 p-3">
        <div class="col-md-12">
          <h2>What I do Today ?</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-lg-12">
          <div class="work-todo">
            <div class="row">
              <div v-for="data in tugas" v-bind:key="data.id" class="mb-3 tugas col-md-12 text-start">
                <div class="form-check">
                  <ItemTugas v-bind:data="data" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div> 
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css';
import ItemTugas from './components/ItemTugas.vue';

export default {
  name: "app",
  components: {
    ItemTugas
  },
  data: function () {
    return {
      tugas: [
        { id: 1, nama: "Work smart 8 hours", isdone: false },
        { id: 2, nama: "Rest smart 8 hours", isdone: false },
        { id: 3, nama: "Pray hard", isdone: false },
        { id: 4, nama: "Learn programming", isdone: false },
        { id: 5, nama: "Playing game", isdone: false },
        { id: 5, nama: "Workout", isdone: false },
        { id: 5, nama: "Playing football", isdone: false },
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.header {
  background: #1abc9c;
}

.header h2 {
  margin: 0;
}

.tugas .item {
  font-size: 20px;
  text-align: left;
}
</style>
