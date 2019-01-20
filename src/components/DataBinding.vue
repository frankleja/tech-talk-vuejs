<template>
    <div class="data-binding">
        <h2>Data Binding</h2>
        <p>current time is {{timestamp}}</p>
        <p>date is {{date}}</p>

        <h3>Attribute binding</h3>
        <a v-bind:href="linkUrl">{{linkText}}</a>

        <h3>Style class binding</h3>
        <p class="fett" v-bind:class="{ big: isBig, red: isRed }">ein Beispieltext</p>

        <button v-on:click="isBig ? isBig=false : isBig=true">toggle size</button>
        <button v-on:click="isRed ? isRed=false : isRed=true">toggle red</button>
    </div>
</template>

<script>
export default {
    name: 'DataBinding',
     // observable data 
    data () {
        return {
            timestamp: null,
            linkUrl: 'http://www.heise.de/',
            linkText: 'Heise',
            isBig: true,
            isRed: false
        }
    }, 
    // derived data
    computed: {
        date: function () {
            return this.timestamp == null ? null : this.timestamp.toLocaleString().substr(0,9)
        }
    },
    // lifecycle hook
    created: function () {
        this.setCurrentTime()
    },
    // all component functions
    methods: {
        setCurrentTime() {
            this.timestamp = new Date().toLocaleString()
        }
    }
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

