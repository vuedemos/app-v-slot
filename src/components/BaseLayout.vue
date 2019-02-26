<template>
    <div class="container">
        <header>
            <slot name="header">Header Content</slot>
        </header>
        <main>
            <slot>Main Content</slot>
        </main>
        <footer>
            <slot name="footer">Footer Content</slot>
        </footer>
    </div>
</template>

<script>
export default {
    name: 'BaseLayout'
}
</script>

<style scoped>

</style>
