<template>
    <div>
        <Notice />
        <div class="notice">
            123123123
        </div>
    </div>
</template>

<script>
import Notice from "./pages/Notice";

export default {
    name: 'App',
	components: {Notice},
}
</script>

<style lang="scss">
$Color-Black: #000;
.notice {
    border: 1px solid $Color-Black;
}
</style>
