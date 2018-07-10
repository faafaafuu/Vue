<template>
    <div class="car">
        <h3>Name: {{carName}}</h3>
        <p>Year: {{carYear}}</p>
        <button @click="changeName">changeName</button>
        <button @click="changeFunc()">changeFunc</button>

    </div>
</template>
<script>
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
        }
    }
}
</script>

<style>
.car {
    border: 1px solid black;
}

</style>
