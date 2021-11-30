<template>
    <div>
        <h1>Proveedores</h1>
        

<table class="table">
<thead class="thead-dark">
<tr>
<th scope="col">Id</th>
<th scope="col">Ruc</th>
<th scope="col">Nombre</th>
<th scope="col">Direccion</th>
<th scope="col">Telefono</th>
</tr>
</thead>
<tbody>
<tr v-for="proveedor in proveedores" :key="proveedor.id" >
<td>{{proveedor.id}}</td>
<td>{{proveedor.ruc}}</td>
<td>{{proveedor.nombre}}</td>
<td>{{proveedor.direccion}}</td>
<td>{{proveedor.telefono}}</td>

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
        proveedores:[]
    }
    },
    methods:{
        async getProveedores(){
        const resp =  await axios.get('http://localhost:8080/api/v1/proveedores');
        this.proveedores= resp.data;
        }
    },
    mounted(){
        this.getProveedores();
    }
    
}
</script>
