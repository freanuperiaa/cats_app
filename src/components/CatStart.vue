<template>
    <div class="cat-start">
        <h3>Oh no! You haven't started a game yet. It's time to have your cat! ^^</h3>
        <b-form>
            <b-form-group
                id="input-group-1"
                label="Cat Name:"
                label-for="input-1"
                description="What's the name of your precious cat?"
            >
                <b-form-input
                id="input-1"
                type="text"
                required
                placeholder="Enter Cat name..."
                ></b-form-input>
            </b-form-group>
        </b-form>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .cat-start {
        margin: 30px;
    }
</style>