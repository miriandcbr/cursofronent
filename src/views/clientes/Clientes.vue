<template>
    <div>
        <h1>Clientes</h1>
        

<table class="table">
<thead class="thead-dark">
<tr>
<th scope="col">Id</th>
<th scope="col">Cedula</th>
<th scope="col">Nombre</th>
<th scope="col">Telefono</th>
</tr>
</thead>
<tbody>
<tr v-for="cliente in clientes" :key="cliente.id" >
<td>{{cliente.id}}</td>
<td>{{cliente.cedula}}</td>
<td>{{cliente.nombre}}</td>
<td>{{cliente.telefono}}</td>
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
        clientes:[]
    }
    },
    methods:{
        async getClientes(){
        const resp =  await axios.get('http://localhost:8080/api/v1/clientes');
        this.clientes= resp.data;
        }
    },
    mounted(){
        this.getClientes();
    }
    
}
</script>
