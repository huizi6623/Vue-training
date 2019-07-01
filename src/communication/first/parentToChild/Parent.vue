<template>
    <div class="parent">
        <h2>父组件向子组件传值</h2>
        <Child :message="message"/>
    </div>
</template>

<script>
    import Child from './Child'
    export default {
        name: 'parent',
        components: {
            Child
        },
        data() {
            return {
                message: '父组件传过去的值'
            }
        }
    }
</script>
