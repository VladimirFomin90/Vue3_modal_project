<template>
    <h1>{{ title }}</h1>
    <br />
    <div v-if="showModal">
        <Modal theme="sale" @close="toggleModal">
            <h1>DarkNet</h1>
            <p>
                Conducting DarkNet-related research will expose you to obscene
                and graphic material. Please proceed with caution
            </p>
        </Modal>
    </div>
    <button @click="toggleModal">Open modal</button>
</template>

<script>
import Modal from './components/Modal.vue';

export default {
    name: 'App',
    components: { Modal },
    data() {
        return {
            title: 'My first Vue App',
            showModal: false,
        };
    },
    methods: {
        toggleModal() {
            this.showModal = !this.showModal;
        },
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #3b4252;
    margin-top: 60px;
}
h1 {
    display: inline-block;
    padding-bottom: 10px;
    border-bottom: 2px solid #ddd;
}
</style>
