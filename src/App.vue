<template>
    <div>
<!--        <Notice />-->
        <Bind />
<!--        <div class="notice">-->
<!--            123123123-->
<!--        </div>-->
    </div>
</template>

<script>
import Notice from "./pages/Notice";
import Bind from "./pages/Bind";

export default {
    name: 'App',
	components: { Notice, Bind},
}
</script>

<style lang="scss">
$Color-Black: #000;
.notice {
    border: 1px solid $Color-Black;
}
</style>
