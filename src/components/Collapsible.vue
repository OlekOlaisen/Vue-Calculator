<!-- Slots -->


<template>

    <section class="collapsible">
        <button @click="toggleCollapse" class="collapsible__button">
            <span>{{ title }}</span>
            <span>+</span>
        </button>
        <div v-if="isCollapsed === false" class="collapsible__content">
            <slot />
        </div>
    </section>
</template>

<script>
export default {

    props: {
        title: {
            type: String
        }
    },


    data() {
        return {
            isCollapsed: true
        }
    },

    methods: {
        toggleCollapse() {
            this.isCollapsed = !this.isCollapsed;
        }
    }
}
</script>


<style scoped>
.collapsible {
    border: 2px solid yellow;
    background-color: black;
    color: white;
    margin-top: 1rem;
    width: 30%;
}

.collapsible__button {
    width: 100%;
    cursor: pointer;
    border: 0;
    display: flex;
    justify-content: space-between;

    background-color: black;
    color: white;
}

.collapsible__button:hover {
    background-color: yellow;
    color: black;
}

.collapsible__button,
.collapsible__content {
    padding: 10px;
}

img {
    width: 300px;
}

p {
    font-size: 1.5rem;
}

span {
    font-size: 1.5rem;
}
</style>