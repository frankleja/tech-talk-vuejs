<template>
    <div class="data-binding">
        <h2>Data Binding</h2>
        <p>current time is {{timestamp}}</p>


        <h3>Attribute binding link</h3>

 
        <h3>CSS class binding</h3>


    </div>
</template>

<script>
export default {
    name: 'DataBinding',
     // observable data 
    data () {
        return {
            timestamp: null,
        }
    }, 
    // all component functions
    methods: {
        setCurrentTime() {
            this.timestamp = new Date().toLocaleString()
        }
    },
};
</script>

<style scoped>
    .big {
        font-size: 20px;
    }
    .red {
        color: red;
    }
    .fett {
        font-weight: bolder;
    }
</style>

