<template>
    <div class="filter">
        <div class="filter__container"> 
            <div class="filter__head">
                <h2 class="title">Filters</h2>
            </div>
            <div class="filter__content">
                <div class="filter__nav">
                    <ul>
                        <li class="filter_item">
                            <i class="fa fa-search"></i>
                            search
                        </li>
                        <li class="filter_item">
                            <i class="fa fa-star"></i>
                            favorites
                        </li>
                        <li class="filter_item">
                            <i class="fa fa-check-circle"></i>
                            complete
                        </li>
                        <li class="filter_item">
                            <i class="fa fa-trash"></i>
                            deleted
                        </li>
                    </ul>
                </div>
                <div class="filter__footer">
                    <div class="underline"></div>
                    <div class="copyright">
                        Dyovana Menegatti
                    </div>
                </div>
                </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Filters',
}
</script>

<style scoped>
@import '@/assets/styles/vars.css';

.filter__container {
    background-color: var(--secondary);
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    padding: 20px;
    margin-top: 15px;
    border-radius: 10px;
    height: 70vh;
    width: 30vw;
}

.title {
    color: var(--primary);
}

.filter__content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    align-items: start;
    width: 100%;
}
.filter__nav ul {
    list-style-type: none;
    margin-top: 15px;
}

.filter__nav li {
    margin-top: 10px;
    color: var(--tertiary);
    font-size: 0.8rem;
    font-weight: 600;
    cursor: pointer;
}

.filter__nav li .fa {
    padding-right: 5px;
}

.filter__footer {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    gap: 10px;
}

.underline {
    width: 100%;
    height: 1px;
    background: var(--general-text);
}

.copyright {
    text-align: center;
    font-size: 0.7rem;
}
</style>