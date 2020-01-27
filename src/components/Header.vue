<template>
    <div class="header">
    <b-navbar toggleable="lg" type="dark" variant="info">
        <b-navbar-brand href="#">Cats!</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
        <template v-if="isInitialized">
            <b-navbar-nav>
                <b-nav-item
                    @click="changepage('app-care')"
                >
                    Care
                </b-nav-item>
                <b-nav-item
                >
                    Play
                </b-nav-item>
                <b-nav-item
                >
                    My Cat
                </b-nav-item>
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
        currentPage: String,
        changepage: Function,
    },

}
</script>

<style scoped>

.header {
    position: relative; min-height: 100%; 
}

</style>