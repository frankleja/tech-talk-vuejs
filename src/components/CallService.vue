<template>
    <div class="call-service">
        <h2>Call service</h2>
        <ol>
            <li v-for="event in events">
            {{ event.equipmentName }} is needed in {{event.targetLocation}}
            </li>
        </ol>
      </div>
</template>

<script>
export default {
    name: 'CallService',
    data () {
        return {
            events: []
        }
    },
    methods: {
        retrieveEvents: function () {
            this.$http.get('http://192.168.242.128/erptool/api/v1/events').then(
                function success (response) {
                    this.events = response.body
                },
                function error (response) {
                    // common error handling with mixin
                    console.log('get events xhr error, status code=' + response.status + ', text=' + response.statusText)
                }
            )
        }
    },
    created: function () {
        this.retrieveEvents()
    }
}
</script>

<style>

</style>
