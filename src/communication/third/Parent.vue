<template>
    <div class="parent">
        <h2>$parent和$children</h2>
        <p>父组件中的值： {{parentMessage}}</p>
        <button @click="changeChildMsg">改变子组件中的值</button>
        <Child/>
    </div>
</template>

<script>
    import Child from './Child'
    export default {
        name: 'parent',
        components: {
            Child
        },
        data(){
            return {
                parentMessage: '默认值'
            }
        },
        methods: {
            changeChildMsg: function(){
                this.$children[0].childMessage = "这是父组件改变的"
            }
        }
    }
</script>
