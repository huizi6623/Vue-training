<template>
    <div class="parent">
        <h2>子组件向父组件传值</h2>
        <p>{{messageFromChild}}</p>
        <Child @listenToChildEvent="showMsgFromChild"/>
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
                messageFromChild: '',
            }
        },
        methods: {
            showMsgFromChild: function(msg){
                this.messageFromChild = msg
            }
        }
    }
</script>
