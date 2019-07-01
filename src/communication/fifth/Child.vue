<template>
    <div>
        <p>in child:</p>
        <p>props: {{child}}</p>
        <p>$attrs: {{$attrs}}</p>
        <button @click="changeMsg">改变父组件的值</button>
        <hr>
        <!-- GrandChild组件中能直接触发changeMsg的原因在于 Child组件调用GrandChild组件时 使用 v-on 绑定了$listeners 属性 -->
        <!-- 通过v-bind 绑定$attrs属性，GrandChild组件可以直接获取到Parent组件中传递下来的props（除了Child组件中props声明的） -->
        <GrandChild v-bind="$attrs" v-on="$listeners"></GrandChild>
    </div>
</template>
<script>
    import GrandChild from './GrandChild.vue';
    export default {
        props: ['child'],
        data() {
            return {};
        },
        inheritAttrs: false,
        components: {GrandChild},
        methods: {
            changeMsg: function(){
                this.$emit('changeMsg1', '这是子组件改变的');
            }
        }
    };
</script>
