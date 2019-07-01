<template>
    <div>
        <h2>firstChild组件</h2>
        <button @click="sendMsg">向另一个组件传值</button>
    </div>
</template>

<script>
    import bus from './eventBus'
    export default {
        methods: {
            sendMsg: function(){
                bus.$emit('userDefinedEvent', 'this message is from firstChild')
            }
        }
    }
</script>
