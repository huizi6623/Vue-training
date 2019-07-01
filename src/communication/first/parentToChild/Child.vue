<template>
    <div>
        <h3>child子组件部分</h3>
        <p>{{message}}</p>
    </div>
</template>

<script>
    export default {
        name: 'child',
        props: ['message']
    }
</script>
