<template>
    <div class="notice">
        <ul>
            <NoticeItem
                v-for="info in infos"
                :id="info.id"
                :name="info.name"
                :image="info.image"
                :price="info.price"
                :stock="info.stock"
                :tags="info.tags"
            />
        </ul>
    </div>
</template>

<script>

import axios from 'axios';
import NoticeItem from "../components/NoticeItem";
export default {
    name: 'Notice',
	components: {NoticeItem},
	data() {

        return {
            infos : null,
            infos2 : null
        }

		// return {
		// 	lists: [
        //         {
        //         	id: 0,
        //         	title: '공지사항 제목1',
        //             date: '2019.12.6'
        //         },
		// 		{
		// 			id: 1,
		// 			title: '공지사항 제목2',
		// 			date: '2019.12.6'
		// 		},
		// 		{
		// 			title: '공지사항 제목3',
		// 			date: '2019.12.6'
		// 		},
		// 		{
		// 			title: '공지사항 제목4',
		// 			date: '2019.12.6'
		// 		}
        //     ]
		// }


	},
  mounted (){
      // axios.get('http://localhost:3000/api').then(res => {
      //     this.infos = res.data.beers;
      // })
  }
}
</script>

<style></style>
