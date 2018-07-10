<template>
    <div class="car">
        <h3>Name: {{carName}}</h3>
        <p>Year: {{carYear}}</p>
        <button @click="changeName">changeName</button>
        <button @click="changeFunc()">changeFunc</button>
        <button @click="updateCounter()">updateCounter</button>

    </div>
</template>
<script>
import {eventEmitter} from '../main'
export default {
    props: {
        carName: {
            type: String,
            default: 'default Name'
        },
        carYear: Number,
        changeFunc: Function,
    },
    data() {
        return {
        }
    },
    methods: {
        changeName() {
            this.carName = 'mazda';
            this.$emit('nameChanged', this.carName)//прослушка события
        },
        updateCounter(){
            // this.$emit('counterUpdated', this.counter++)
            eventEmitter.$emit('counterUpdated', 5)
        }
    }
}
</script>

<style>
.car {
    border: 1px solid black;
}

</style>
