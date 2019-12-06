<template>
    <div class="notice">
        <ul>
            <NoticeItem
                v-for="list in lists"
                :title="list.title"
                :date="list.date"
                :key="index"
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
			lists: [
                {
                	id: 0,
                	title: '공지사항 제목1',
                    date: '2019.12.6'
                },
				{
					id: 1,
					title: '공지사항 제목2',
					date: '2019.12.6'
				},
				{
					title: '공지사항 제목3',
					date: '2019.12.6'
				},
				{
					title: '공지사항 제목4',
					date: '2019.12.6'
				}
            ]
		}
	}
}
</script>

<style>

</style>
