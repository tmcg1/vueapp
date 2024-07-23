<template>
    <div class="header">
        <img alt="Logo" src="../assets/agriest.jpg">
        <div class="menus">
            <div @click="scrollToBottom">Müük</div>
            <div @click="scrollToBottom">Kontakt</div>
        </div>
    </div>
</template>
  
<script>
export default {
    name: 'NavBar',
    props: {
        msg: String,
        bottomEl: String
    },
    methods: {
        scrollToBottom() {
            console.log('this.$refs', this.$refs, this.$root.$refs, bottomEl)
            this.$refs.bottomEl?.scrollIntoView({ behavior: 'smooth' });
        },
    },
}
</script>
  
<style scoped>
img {
    width: 200px;
}

.header {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px
}

.menus {
    display: flex;
    gap: 20px
}
</style>
  