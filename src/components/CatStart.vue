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
                v-model="catName"
                ></b-form-input>
            </b-form-group>
            <b-form-group
                id="input-group-2"
                label="Breed:"
                label-for="input-2"
                description="What's his/her breed?"
            >
                <b-form-input
                id="input-2"
                type="text"
                required
                placeholder="Enter Cat breed..."
                v-model="catBreed"
                ></b-form-input>
            </b-form-group>
            <b-form-group
                id="input-group-3"
                label="Cat Age:"
                label-for="input-3"
                description="How old is your cat (in years)?"
            >
                <b-form-input
                id="input-3"
                type="text"
                required
                placeholder="Enter Cat Age..."
                v-model="catAge"
                ></b-form-input>
            </b-form-group>
            <b-form-group
                id="input-group-4"
                label="Description:"
                label-for="input-4"
                description="Describe your cat..."
            >
                <b-form-textarea
                id="input-4"
                type="textarea"
                required
                placeholder="Say something about your cat!"
                v-model="catDescription"
                ></b-form-textarea>
            </b-form-group>
            <b-button variant="primary" @click="createCat(catName, catBreed, catAge, catDescription)"
            >
                Submit
            </b-button>
        </b-form>
    </div>
</template>

<script>
export default {
    props: {
        createCat: Function,

    },
    data: function() {
        return {
            catName: '',
            catBreed: '',
            catAge: 0,
            catDescription: '',
        };
    },
}
</script>

<style scoped>
    .cat-start {
        margin: 30px;
    }
</style>