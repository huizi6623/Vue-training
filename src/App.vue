<template>
    <div id="app">
        <Parent1_parentToChild/>
        <Parent1_childToParent/>

        <div class="parent">
            <h2>总线方式进行平级通信</h2>
            <FirstChild/>
            <SecondChild/>
        </div>

        <Parent3/>
        <Parent4/>
        <Parent5/>
    </div>
</template>

<script>
    import Parent1_parentToChild from './communication/first/parentToChild/Parent'
    import Parent1_childToParent from './communication/first/childToParent/Parent'

    import FirstChild from './communication/second/FirstChild'
    import SecondChild from './communication/second/SecondChild'

    import Parent3 from './communication/third/Parent'

    import Parent4 from './communication/fourth/Parent'

    import Parent5 from './communication/fifth/Parent'

    export default {
        name: 'app',
        components: {
            Parent1_parentToChild,
            Parent1_childToParent,

            FirstChild,
            SecondChild,

            Parent3,
            Parent4,
            Parent5
        }
    }
</script>

<style>
    .parent{
        width: 600px;
        border: 1px solid #ccc;
        margin-bottom: 10px;
        padding: 10px;
    }
</style>

