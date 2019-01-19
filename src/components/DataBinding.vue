<template>
    <div class="data-binding">
        <h2>Data Binding</h2>
        <p>current time is {{timestamp}}</p>
        <p>date is {{date}}</p>
    </div>
</template>

<script>
export default {
    name: 'DataBinding',
     // observable data 
    data () {
        return {
            timestamp: null
        }
    }, 
    // derived data
    computed: {
        date: function () {
            if (this.timestamp == null) {
                return null
            }
            return this.timestamp.toLocaleString().substr(0,9)
        }
    },
    // lifecycle hook
    created: function() {
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
