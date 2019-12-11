<template>
    <div class="notice">
        <ul>
            <NoticeItem
                v-for="list in lists"
                :name="list.name"
                :price="list.price"
                :key="list.id"
                :stock="list.stock"
                :src="list.image"
                :tags="list.tags"
            />
        </ul>
    </div>
</template>

<script>
import NoticeItem from "../components/NoticeItem";
export default {
    name: 'Notice',
	components: {NoticeItem},
	data() {
        return {
            lists: null
        }
    },
    mounted () {
        const axios = require('axios').default;
        axios
            .get('http://localhost:3000/api')
            .then(response => (this.lists = response.data.beers))
            .catch(error => console.log(error))
    }
}
</script>

<style></style>
