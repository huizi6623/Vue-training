<template>
    <div>
        <h3>子组件部分</h3>
        <p>子组件中的值： {{childMessage}}</p>
        <button @click="changeParentMsg">改变父组件中的值</button>
    </div>
</template>

<script>
    export default {
        name: 'child',
        data(){
            return {
                childMessage: '默认值'
            }
        },
        methods: {
            changeParentMsg: function(){
                this.$parent.parentMessage = '这是子组件改变的'
            }
        }
    }
</script>
