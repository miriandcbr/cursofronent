<template>
    <div>
        <h1>Productos</h1>
        

<table class="table">
<thead class="thead-dark">
<tr>
<th scope="col">Id</th>
<th scope="col">Descripcion</th>
<th scope="col">Precio</th>
<th scope="col">Proveedor</th>
<th scope="col">Direccion</th>
</tr>
</thead>
<tbody>
<tr v-for="producto in productos" :key="producto.id" >
<td>{{producto.id}}</td>
<td>{{producto.descripcion}}</td>
<td>{{producto.precio}}</td>
<td>{{producto.proveedor.nombre}}</td>
<td>{{producto.proveedor.direccion}}</td>

</tr>
</tbody>
</table>





    </div>
</template>

<script>
  import axios from 'axios'

export default {
    data(){
    return {
        productos:[]
    }
    },
    methods:{
        async getProductos(){
        const resp =  await axios.get('http://localhost:8080/api/v1/productos');
        this.productos= resp.data;
        }
    },
    mounted(){
        this.getProductos();
    }
    
}
</script>
