<template>
    <div class="btn-new">
        <button class="new-task">new task <i class="fa fa-plus"></i></button>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
@import '@/assets/styles/vars.css';


button {
    border: none;
    background: transparent;
    border: 2px solid var(--background-second);
    border-radius: 20px;
    width: 300px;
    padding: 5px 15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: var(--background-second);
    font-size: 0.8rem;
    cursor: pointer;
}

button:hover {
    background-color: var(--primary);
    border: none;
    color: var(--general-text);
}
</style>