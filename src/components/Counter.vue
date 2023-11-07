<script>
export default {
    name: 'CounterView',
    data() {
        return {
            counter: 0
        }
    },
    methods: {
        submitForm(event) {
            //Prevent a page refresh
            event.preventDefault();
            alert('The form was sumitted')
        },
        countUp() {
            this.counter++
        },
        countDown() {
            this.counter--
        }
    }
}
</script>

<template>
    <div>
        <h1>{{ counter }}</h1>
        <span>
            <button @click.right="countUp">Counter UP</button>
            <button @click.middle="countDown">Counter Down</button>
        </span>
    </div>
    <form @submit.prevent="submitForm">
        <p>
            <button>Submit</button>
        </p>
    </form>
</template>

<style lang="scss" scoped></style>