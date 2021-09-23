<template>
    <h2>Dollar Today</h2>
    <hr>
    <p>FECHA: {{ fecha }}</p>
    <p>PROMEDIO BS.: {{ promedio }}</p>
    <hr>
</template>

<script>
export default {

    data(){
        return{
            fecha: null,
            promedio: null,
        }
    },

    created(){
        this.getInfoDollarToday()
    },

    methods: {
        async getInfoDollarToday(){
            const { USD, _timestamp } = await fetch('https://s3.amazonaws.com/dolartoday/data.json').then( r => r.json() )
            this.fecha = _timestamp.fecha
            this.promedio = USD.promedio
        }
    }
    
}
</script>

<style scoped>
h2, a{
    color: #64BB87;
}
p {
  font-size: 16px;
  font-weight: bold;
  color: white;
}
</style>