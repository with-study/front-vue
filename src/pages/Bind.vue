<template>
    <div>
<!--        <img src="https://upload.wikimedia.org/wikipedia/commons/4/41/Gong_Yoo_%28Sep_2016%29.png" alt="" />-->
        <img v-bind:src="imagePath1" :alt="textAlt1" :class="isActive ? 'active' : ''"/>
        <img v-bind:src="imagePath2" :alt="textAlt2" ref="sdfsdfsdf" />


        <button @click="onChange">가나다</button>
        <button @click="callMoreNotice">더보기</button>
    </div>
</template>

<script>
	export default {
		name: 'Bind',
		data() {
			return {
				imagePath1: "https://upload.wikimedia.org/wikipedia/commons/4/41/Gong_Yoo_%28Sep_2016%29.png",
				imagePath2: "https://upload.wikimedia.org/wikipedia/commons/d/dc/190501_%EC%A0%95%EC%9A%B0%EC%84%B1.jpg",
                textAlt1: "공유",
                textAlt2: "정우성",
                isActive: false,
            }
		},
        created() {
			this.callMoreNotice();
		},
		methods: {
			onChange() {
				this.isActive = !this.isActive
            },
        }
	}
</script>

<style>
.active {
    border: 2px solid hotpink;
}
</style>
