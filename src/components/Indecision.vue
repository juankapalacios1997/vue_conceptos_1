<template>
    <img src="https://via.placeholder.com/250" alt="sample-img" />
    <div class="bg-dark"></div>
    <div class="indecision-container">
        <input type="text" placeholder="Hazme una pregunta" v-model="question" />
        <p>Recuerda terminar con un signo de interrogación (?)</p>
        <div>
            <h2>Seré millonario?</h2>
            <h1>Sí... No... Pensando</h1>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Indecision',
    data() {
        return {
            question: ''
        }
    },
    watch: {
        question(value, oldValue) {
            console.log(value.includes('?'))
        }
    }

}
</script>

<style scoped>
    img, .bg-dark {
        height: 100vh;
        left: 0px;
        max-height: 100%;
        max-width: 100%;
        position: fixed;
        top: 0px;
        width: 100vw;
    }

    .bg-dark {
        background-color: rgba(0, 0, 0, 0.4);
    }

    .indecision-container {
        position: relative;
        z-index: 99;
    }
    
    input {
        width: 250px;
        padding: 10px 15px;
        border-radius: 5px;
        border: none;
    }
    input:foch1us {
        outline: none;
    }

    p {
        color: white;
        font-size: 20px;
        margin-top: 0px;
    }

    h1, h2 {
        color: white;
    }
    
    h2 {
        margin-top: 150px;
    }

</style>