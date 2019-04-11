<template>
    <div class="home">
        <HelloWorld msg="Welcome to Your Vue.js App"/>
        <about :val='val' :head="val" @click="alert">
            <div slot="ttt" slot-scope="user1">
                <div>替换了吗{{JSON.stringify(user1)}}</div>
            </div>
            <div slot="head">我来组成头部</div>
            <div slot="leg">我来组成大腿</div>
        </about>
    </div>
</template>
<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import About from './About.vue'

export default {
    name: 'home',
    components: {
        HelloWorld, About
    },
    data() {
        return {
            text: 120,
            val: 12
        }
    },
    methods: {
        alert: function() {
            alert(1)
        }
    }
}
</script>
