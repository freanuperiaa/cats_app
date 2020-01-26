<template>
    <div class="header">
    <b-navbar toggleable="lg" type="dark" variant="info">
        <b-navbar-brand href="#">Cats!</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
        <template v-if="isInitialized">
            <b-navbar-nav>
                <b-nav-item href="#">Link</b-nav-item>
                <b-nav-item href="#">Disabled</b-nav-item>
            </b-navbar-nav>
        </template>

        </b-collapse>
    </b-navbar>
    </div>
</template>

<script>
export default {
    props: {
        isInitialized: Boolean,
    },

}
</script>

<style scoped>

.header {
    position: relative; min-height: 100%; 
}

</style>