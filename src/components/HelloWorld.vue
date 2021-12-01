<template>

     <div>
         <h1>Aplicacion curso Web </h1>
         Aplicacion de Back end usuando Spring Boot y para 
          el  Front end  se ua VUE <p/>
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
        clientes:[{id:1,nombre:'Mirian'},{id:2,nombre:'Carmen'}],
        url:"http://www.google.com",
        numero1:0,
        numero2:0,
        resultado:0,
        tarea:null,
        tareas:['descripcion']
      }
    },
methods :{
      metodo1(){
        alert('Ingresa a l metodo');
        },
        sumar(){
          this.resultado=this.numero1+this.numero2;
        },

         restar(){
          this.resultado=this.numero1-this.numero2;
        },

         multiplicar(){
          this.resultado=this.numero1*this.numero2;
        },
        dividir(){
          this.resultado=this.numero1/this.numero2;
        },
        agregarTarea(){
          this.tareas.push(this.tarea);
        }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  color:cadetblue;
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
