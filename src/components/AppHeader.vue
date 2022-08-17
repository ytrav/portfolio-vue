<template>
    <header>
        <h2>Anton Shevchuk</h2>
    </header>
</template>

<style lang="scss" scoped>
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

a {
    text-decoration: none;
    color: inherit;
}

header {
    display: flex;
    position: absolute;
    top: 60px;
    left: 60px;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    color: $primary;
    #anchors {
        display: flex;
        justify-content: space-between;
        justify-items: flex-start;
        align-items: center;
        flex-wrap: wrap;
        gap: 5px;
    }
}

</style>