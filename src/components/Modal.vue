<script>
export default {
    props: ['theme'],
    methods: {
        closeModal() {
            this.$emit('close');
        },
    },
};
</script>

<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{ sale: theme === 'sale' }">
            <slot></slot>
        </div>
    </div>
</template>

<style>
.modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: #d8dee9;
    border-radius: 10px;
}
.backdrop {
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
}
.modal h1 {
    color: rgb(92, 177, 92);
}
.modal.sale {
    background: red;
    color: white;
}
.modal.sale h1 {
    color: aliceblue;
}
</style>
