<template>
    <div class="todo">
        <div class="todo__container">
            <div class="todo__header">
                <div class="header-title">
                    <h1><span class="mode_title">to</span>do.</h1>
                </div>

                <div class="header-btn">
                    <i class="fa fa-sun-o" @click="handleMode" v-if="modeChange"></i>
                    <i class="fa fa-moon-o" @click="handleMode" v-else></i>
                </div>
            </div>

            <div class="todo__content">
                <Filters></Filters>
            </div>
        </div>
    </div>
</template>

<script>
import Filters from '@/components/Filter';

export default {
    name: 'ToDo',
    components: { Filters, },
    data() {
        return {
            modeChange: true,
        }
    },
    methods: {
        handleMode() {
            this.modeChange = !this.modeChange;
        },
    },
}
</script>

<style scoped>
@import '@/assets/styles/vars.css';

.todo__container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width: 80vw;
    height: 80vh;
}

.todo__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
}

.header-title {
    color: var(--primary);
}

.mode_title {
    color: var(--general-text);
}

.header-btn .fa {
    cursor: pointer;
}
</style>