<template>
    <div class="tasks">
        <div class="tasks__container">
            <div class="tasks__head">
                <h2 class="title">Tasks</h2>
            </div>
            <div class="tasks__content">
                <div class="btn">
                    <ButtonNew></ButtonNew>
                </div>

                <div class="task">
                    <div class="task__item">
                        <i class="fa fa-circle-thin"></i>
                        <label for="">Item 1</label>
                    </div>
                    <div class="task__actions">
                        <i class="fa fa-star"></i>
                        <i class="fa fa-pencil"></i>
                        <i class="fa fa-trash"></i>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ButtonNew from '@/components/ButtonNew';

export default {
    components: { ButtonNew, }    
}
</script>

<style scoped>
@import '@/assets/styles/vars.css';


.tasks__container {
    background-color: var(--secondary);
    padding: 20px 35px;
    margin-top: 15px;
    border-radius: 10px;
    height: 70vh;
    width: 50vw;
}

.title {
    color: var(--primary);
}

.tasks__content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
}

.btn {
    padding: 20px 0px 10px 0px;
}

.task {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    background-color: var(--background-second);
    border-radius: 6px;
    padding: 5px 25px;
    font-size: 0.9rem;
}

.task__item .fa {
    margin-right: 10px;
    cursor: pointer;
}

.task__actions {
    display: flex;
    gap: 10px;
}

.task__actions .fa {
    cursor: pointer;
}
</style>