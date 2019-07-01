<template>
    <div>
        <h3>child子组件部分</h3>
        <button @click="sendMsgToParent">向父组件传值</button>
    </div>
</template>

<script>
    export default {
        name: 'child',
        methods: {
            sendMsgToParent: function(){
                this.$emit('listenToChildEvent', '这是向父组件传递的消息！')
            }
        }
    }
</script>
