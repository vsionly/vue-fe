<template>
    <div class="about">
        <slot name="leg">1111111111</slot>
        <slot name="head">222222222</slot>
        <slot name="ttt" a=2 d=3 :user="text1">默认的那个</slot>
        <slot name="leg">1111111111</slot>
        <h1 v-if="val==120">{{head}}</h1>
    </div>
</template>
<script>

export default {
    name: 'about',
    props: {
        head: {
            type: Number,
            default: 0
        },
        val: {
            default: 0
        }
    },
    data(){
        return {
            text1: {
                a: 99,
                b: 66
            }
        }
    },
    methods: {
        alert() {
            alert(41)
        }
    }
}
</script>