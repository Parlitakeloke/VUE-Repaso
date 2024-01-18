<template>
    <h1>HOLA MUNDO CON VUE</h1>
    <input type="text" name="fruta" id="campoFruta" v-model="frutika">
    <button @click="agregarFruta">Agregar</button>
    <ul>
        <li v-for="(fruta, index) in frutas">
            {{ index }} - {{ fruta.nombre }}
            <small>({{ fruta.cantidad }}) <p v-if="fruta.cantidad <= 0">Sin Stock</p></small>
        </li>
    </ul>

    <h1>TOTAL: </h1>
</template>

<script>
export default {
    name: 'Ejercicio1',
    components: {},
    data() {
        return {

            frutas: [
                { nombre: 'Pera', cantidad: '10' },
                { nombre: 'Manzana', cantidad: '20' },
                { nombre: 'Patata', cantidad: '0' },
            ],
            frutika : ""
            
        }
    },
    methods: {

        agregarFruta(){

            let objetiko =  {nombre: this.frutika, cantidad: 0};
            this.frutas.push(objetiko);

        }

    }
}
</script>