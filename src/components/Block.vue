<template>
    <div class="block">
        click me
    </div>
</template>

<script>
    export default {
        props:['delay']
    }
</script>

<style>

.block {
    width: 400px;
    height: 50px;
    border-radius: 20px;
    color: white;
    background-color: #6af953;
    text-align: center;
    justify-content: center;
    padding: 100px auto;
    margin: 40px auto;
}

</style>