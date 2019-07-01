<template>
    <div>
        <p>in child:</p>
        <p>props: {{child}}</p>
        <p>$attrs: {{$attrs}}</p>
        <button @click="changeMsg">改变祖先组件的值</button>
        <hr>
        <!-- C组件中能直接触发changeMsg的原因在于 B组件调用C组件时 使用 v-on 绑定了$listeners 属性 -->
        <!-- 通过v-bind 绑定$attrs属性，C组件可以直接获取到A组件中传递下来的props（除了B组件中props声明的） -->
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
        components: {
            GrandChild
        },
        methods: {
            changeMsg: function(){
                this.$emit('changeMsg1', '这是子组件改变的');
            }
        }
    };
</script>
