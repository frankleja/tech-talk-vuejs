<template>
    <div class="call-service">
        <h2>Call service 3</h2>
        <ol>
            <li v-for="event in events">
            {{ event.equipmentName }} is needed in {{event.targetLocation}}
            </li>
        </ol>
      </div>
</template>

<script>
import axios from "axios"

export default {
    name: 'CallService',
    data () {
        return {
            events: []
        }
    },
    created () {
        axios.get('http://192.168.242.128/erptool/api/v1/events')
        .then(function (response) {
                this.events = response.data
        })
        .catch(function (error) {
            // common error handling with mixin
            console.log('axios error' + error)
        })
    }    
}
</script>

<style>

</style>
