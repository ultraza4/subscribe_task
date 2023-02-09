<template>
    <div class="alert">
        <div class="success" v-if="alertType == 'success'">
            <span>You have successfully subscribed to the newsletter</span>
            <Icon icon="ph:x" class="close-btn" @click="$emit('closeAlert')"/>
        </div>
        <div class="error" v-if="alertType == 'error'">
            <span>You have already subscribed to the newsletter</span>
            <Icon icon="ph:x" class="close-btn" @click="$emit('closeAlert')"/>
        </div>
    </div>
</template>

<script>
import { Icon } from '@iconify/vue';

export default {
    emits: ['closeAlert'],
    props: {
        alertType: String,
    },
    components: {
        Icon
    }
}

</script>

<style lang="scss" scoped>
.alert {
    display: flex;
    font-size: 0.8rem;
    position: absolute;
    top: 390px;
    left: 150px;
    color: white;

    .success {
        display: flex;
        width: 200px;
        align-items: center;
        padding: 5px;
        border-radius: 15px;
        background-color: rgb(28, 196, 28);
    }

    .error {
        display: flex;
        width: 200px;
        align-items: center;
        padding: 5px;
        background-color: rgb(228, 57, 57);
        border-radius: 15px;
    }
    .close-btn{
        width: 25px;
        cursor: pointer;
    }
}
</style>