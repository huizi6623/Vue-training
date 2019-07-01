<template>
    <div class="parent">
        <h2>$attrs和$listeners</h2>
        <p>父组件中的两个值：</p>
        <p>子组件会改变的值：{{message1}}</p>
        <p>孙子组件会改变的值：{{message2}}</p>
        <hr>
        <!--        此处监听了两个事件，可以在B组件或者C组件中直接触发-->
        <child1 :child="child" :grand-child="grandChild" v-on:changeMsg1="changeMsg1" v-on:changeMsg2="changeMsg2"/>
    </div>
</template>
<script>
    import Child1 from './Child.vue'

    export default {
        data() {
            return {
                child: 'child',
                grandChild: 'grandChild',
                message1: '默认值',
                message2: '默认值'
            };
        },
        components: {Child1},
        methods: {
            changeMsg1(msg) {this.message1 = msg},
            changeMsg2(msg) {this.message2 = msg}
        }
    };
</script>
