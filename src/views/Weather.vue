<template>
    <div>
        날씨정보
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue'
    import axios from 'axios'
    export default defineComponent({
        mounted(){
            this.getWeahterData()
        },
        methods: {
            getWeahterData() {
                axios.get(
                    'http://api.weatherstack.com/current?access_key=b132237f785961568ee9e17b3ba8d491&query=Seoul'
                    ).then((Res) => {
                    console.log(Res)
                })
            }
        }
    })
</script>