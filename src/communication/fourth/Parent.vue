<template>
    <div class="parent">
        <h2>Provide和inject</h2>
        <Child />
    </div>
</template>

<script>
    import Child from './Child'
    export default {
        name: 'parent',
        provide: {
            name: 'Garrett'
        },
        components: {
            Child
        }
    }
</script>
