<template>
    <div class="block" v-if="showBlock">
        Click me
    </div>
</template>
<script>
export default {
    props: ['delay'],
    data(){
        return {
            showBlock: false
        }
    },
    mounted(){
        console.log("The component has been mounted :)")
        setTimeout(() => { 
            this.showBlock = true;
        }, this.delay)
    },
    updated(){
        console.log("The component has been updated :)")
    }
}
</script>
<style scoped>
    .block{
        width: 400px;
        border-radius:  20px;
        background: #0faf87;
        color: white;
        text-align: center;
        padding: 100px 0;
        margin: 40px auto;
    }
</style>