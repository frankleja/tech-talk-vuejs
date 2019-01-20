<template>
    <div class="input-binding">
        <h2>Input Binding</h2>
        <h3>Text field</h3>
        <input id="text" v-model.trim="form.text" placeholder="edit me">
        <label for="text">Message is: {{ form.text }}|</label>

        <h3>Number field</h3>
        <input id="number" type="number" v-model.number="form.number" >
        <label for="number">Number is: {{ form.number }}</label>

        <h3>Checkbox</h3>
        <input type="checkbox" id="checkbox" v-model="form.checkbox">
        <label for="checkbox">state {{ form.checkbox }}</label>

        <h3>Drop down list</h3>
        <select id="singleSelect" v-model="form.singleSelect">
        <option disabled value="">Please select one</option>
        <option>A</option>
        <option>B</option>
        <option>C</option>
        </select>
        <label for="singleSelect">Selected: {{ form.singleSelect }}</label>

        <h3>Text area</h3>
        <textarea v-model="form.message" placeholder="add multiple lines"></textarea>
        <p class="preformatted">{{ form.message }}</p>
        <button v-on:click="form.message='inline'">clear inline</button>
        <button @click="clearMessage">clear method</button>
    </div>
</template>

<script>
export default {
    name: 'InputBinding',
    data () {
        return {
            form: {
                text: 'start', 
                number: 1,
                checkbox: true,
                singleSelect: 'A',
                message: 'erste Zeile\nZeile 2'
            }
        }
    },
    methods: {
        clearMessage() {
            this.form.message = 'method'
        }
    }
}
</script>

<style scoped>
    .preformatted {
        white-space: pre-line;
    }
</style>
