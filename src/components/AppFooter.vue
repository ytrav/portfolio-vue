<template>
    <footer>
        <p>Anton Shevchuk</p>
        <p>front-end developer</p>
        <a href="#">back to top</a>
    </footer>
</template>

<style lang="scss" scoped>
$primary: #00315f;
$bg1: #efffff;
$bg2: #e3f5f7;

footer {
    margin-top: 100px;
    padding: 60px;
    background-color: $primary;
    color: $bg1;
    text-align: center;
    display: flex;
    flex-direction: column;
    gap: 20px;
}

a {
    color: $primary;
    background-color: $bg1;
    text-decoration: none;
    margin-top: 15px;
    text-align: center;
    align-self: center;
    border: 2px solid $bg1;
    border-radius: 5000px;
    width: 200px;
    padding: 5px 20px 5px 20px;
    transition: background-color 0.2s ease-out;
    &:hover {
        background-color: $primary;
        color: $bg1;
    }
}

</style>