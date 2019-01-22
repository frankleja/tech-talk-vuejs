<template>
    <div class="data-binding">
        <h2>Data Binding</h2>
        <p>current time is </p>
        <p>date is </p>

        <h3>Attribute binding</h3>
        <a ></a>

        <h3>CSS class binding</h3>
        <p class="fett" >ein Beispieltext</p>

        <button >toggle size</button>
        <button >toggle red</button>
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

