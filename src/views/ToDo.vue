<template>
    <div class="todo">
        <div class="todo__container">
            <div class="todo__header">
                <div class="header__title">
                    <h1><span class="title">to</span>do.</h1>
                </div>

                <div class="header__btn">
                    <i class="fa fa-sun-o" @click="toggleDarkLightMode" v-if="darkLightMode"></i>
                    <i class="fa fa-moon-o" @click="toggleDarkLightMode" v-else></i>
                </div>
            </div>

            <div class="todo__content">
                <Filters
                    class="content__filter"
                ></Filters>

                <Tasks
                    class="content__tasks"
                ></Tasks>
            </div>

            <div class="todo__footer">
                <div class="underline"></div>
                <div class="copyright">
                    Dyovana Menegatti
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Filters from '@/components/Filter';
import Tasks from '@/components/Tasks';

export default {
    name: 'ToDo',
    components: { Filters, Tasks, },
    data() {
        return {
            darkLightMode: true,
        }
    },
    methods: {
        toggleDarkLightMode() {
            this.darkLightMode = !this.darkLightMode;
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

.header__title {
    color: var(--primary);
}

.title {
    color: var(--general-text);
}

.header__btn .fa {
    cursor: pointer;
}

.todo__content {
    display: flex;
    justify-content: space-between;
    align-items: stretch;
    width: 100%;
    gap: 20px;
}

.todo__footer {
    width: 100%;
    display: none;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    gap: 10px;
}

.underline {
    width: 100%;
    height: 1px;
    background: var(--tertiary);
}

.copyright {
    text-align: center;
    font-size: 0.7rem;
    color: var(--tertiary);
}

@media screen and (max-width: 550px) {
    .content__filter {
        display: none;
    }

    .todo__footer {
        margin-top: 20px;
        display: flex;
    }
}
</style>