<template>
  <div id="app">
    <table >
      <tr>
        <td>
          <input type="number" v-model="nombre[0]" v-on:change="colorChange">
        </td>
        <td>
          Rouge
        </td>
      </tr>
      <tr>
        <td>
          <input type="number" v-model="nombre[1]" v-on:change="colorChange">
        </td>
        <td>
          Vert
        </td>
      </tr>
      <tr>
        <td>
          <input type="number" v-model="nombre[2]" v-on:change="colorChange">
        </td>
        <td>
          Bleue
        </td>
      </tr>
    </table>
    <div id="color"></div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      nombre: [0, 0, 0],
    };
  },
  methods: {
    colorChange() {
      const colorPick = document.getElementById('color');
      colorPick.style.background = `rgb(${this.nombre[0]}, ${this.nombre[1]}, ${this.nombre[2]})`;
    },
  },
};
</script>

<style lang="scss">
#color{
  height: 176px;
  width : 176px;

  background-color: black;
}
</style>
