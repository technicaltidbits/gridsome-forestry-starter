<template>
    <footer class="footer">
        <div class="container">
            <span v-html="settings.footer" />
            <p>Read my <a href="https://www.technicaltidbits.net/release-notes">release notes.</a></p>
        </div>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            settings: require("../../data/theme.json")
        }
    }
}
</script>

<style scoped>
.footer {
    font-size: 0.8rem;
    padding: 6rem 0;
}
</style>
