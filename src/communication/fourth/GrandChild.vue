<template>
    <div>
        <h3>孙子组件部分</h3>
        <p>{{name}}</p>
    </div>
</template>

<script>
    export default {
        name: 'grandChild',
        inject: ['name'],
    }
</script>
