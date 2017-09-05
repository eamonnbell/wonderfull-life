<template>
    <div class="wonderfull" v-bind:style="computedStyle">
        {{ message }}</div>
</template>
<script>
export default {
    name: 'wonderfull-life',
    props: {
        message: {
            default: '',
            type: String,
        }
    },
    data() {
        return {
            top: 52 + Math.random() * 480,
            left: Math.random() * 480,
            fontSize: 12 + Math.random() * 50
        };
    },
    computed: {
        computedStyle() {
            return {
                top: this.top + 'px',
                left: this.left + 'px',
                'font-size': this.fontSize + 'px',
            };
        }
    }
}
</script>
<style scoped>
div.wonderfull {
    position: absolute;
    font-family: sans-serif;
    color: rgba(0, 0, 0, 0.5);
    user-select: none;
}
</style>
