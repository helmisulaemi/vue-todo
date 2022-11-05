<template>
  <div>
    <input class="form-check-input" v-on:click="rubahTodo()" type="checkbox" id="gridCheck">
    <label class="form-check-label item" v-bind:class="{'item-complated': datas.isdone}" for="gridCheck">
        {{ datas.nama }}
    </label>
  </div>
</template>

<script>
export default {
    name: 'ItemTugas',
    props: ["data"],
    data: function () {
      return {
        datas: this.data
      }
    },
    methods: {
      rubahTodo: function() {
        this.datas.isdone = !this.datas.isdone;
      }
    }
}
</script>

<style scoped>
.item-complated {
  color: #1abc9c;
}
</style>