<template>
    <div>
        <p>in grandChild:</p>
        <p>props: {{grandChild}}</p>
        <p>$attrs: {{$attrs}}</p>
        <button @click="changeMsg">改变祖先组件的值</button>
    </div>
</template>
<script>
    export default {
        props: ['grandChild'],
        data() {
            return {};
        },
        inheritAttrs: false,
        methods: {
            changeMsg: function(){
                this.$emit('changeMsg2', '这是孙子组件改变的');
            }
        }
    };
</script>
