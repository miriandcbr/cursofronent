<template>
  
   <div >
     {{nombre}}
    <ul>
      <li v-for="item in clientes" :key="item.id">
              {{item.nombre}}

      </li>
    </ul>
    </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return{
        nombre:'Alex',
        mostrar:true,
        clientes:[{id:1,nombre:'Mirian'},{id:2,nombre:'Carmen'}]
      }
    },
methods :{
      metodo1(){
        console.log('Ingresa a l metodo');
        }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  color:blue;
  font-weight: bold;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
li{
  color:#42b983;
  font-size:34px
}
</style>
