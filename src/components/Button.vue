<template>
        <button>{{ text }}</button>
</template>

<script>
    export default {
        props: ['text']
    }
</script>

<style lang="scss">
    $yellow: #FCB72B;

        button {
        width: 180px;
        height: 53px;
        background-color: $yellow;
        color: #FFF;
        border: none;
        
        cursor: pointer;
        transition: background-color .5s ease, color .5s ease;
        &:hover {
            background-color: transparent;
            border: solid $yellow 1px;
            color: $yellow;
            
        }

    }


   
    
</style>

