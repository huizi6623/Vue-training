<template>
    <div>
        <h2>secondChild组件</h2>
        <p>从firstchild接收的字符串参数： {{message}}</p>
    </div>
</template>

<script>
    import bus from './eventBus'
    export default {
        data() {
            return {
                message: "默认值"
            }
        },
        mounted() {
            var self = this
            bus.$on('userDefinedEvent', function(msg){
                self.message = msg
            })
        }
    }
</script>
