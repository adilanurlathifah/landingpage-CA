<template>
    <div>
        <aside class="contact">{{ message }}</aside>
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: 'Kontak Kami'
        }
    }
}
</script>

<style>

aside {
    position: fixed;
    top: 40vh;
    z-index: 2;
    inset-block: 0;
    inset-inline-end: 0;
}

aside .contact {
    height: 17%;
    width: 75px;
    display: flex;
    margin-top: 230px;
    border-top-left-radius: 12px;
    border-bottom-left-radius: 12px;
    background-color: #004ECB;
    color: white;
    font-family: 'RobotoBold', sans-serif;
    font-weight: 600;
    font-size: 14px;
    line-height: 23px;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
    gap: 1.5rem;
}

</style>