<template>
    <div>
        <p>{{message}}</p> <!--representar expresiones/var-->
        <p v-show="true">Texto de muestra</p><!-- si ponemos a false se oculta se va a renderizar en nuestro componente-->
        <p v-if="num < 10" > texto con v-if</p>
        <p v-else> Este es el texto v-else</p>
        <ul>
            <li v-for="item in items">{{ item }}</li> <!--array de items-->
        </ul>
        <p>Nombre:</p>
        <input v-model="name" type="text"/>{{name}}
        <button v-on:click="saludo" class="button is-info">SALUDO</button>
    </div>
</template>
<script>
export default {
    //definir modelo de datos
    //http://localhost:3000/directivas
    data(){
        return{
            message:"Hola OpenWebinars",
            num:5,
            items:[1,2,3,4,5,6],
            name: ''
        }
    },
    methods: {
        saludo(){
            console.log("Esto es un saludo")
        }
    }
}
</script>