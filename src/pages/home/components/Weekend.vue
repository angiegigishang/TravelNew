<template>
	<div>
		<div class="title">周末去哪儿</div>
		<ul>
			<li class="item border-bottom" 
			    v-for="item of recommendList"
			    :key="item.id">
			    <div class="item-img-wrapper">
			    	<img class="item-img" :src='item.imgUrl'/>
			    </div>			
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
				</div>				
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: 'HomeWeekend',
	data () {
		return {
				recommendList: [{
				id: '0001',			
				imgUrl: 'https://imgs.qunarzz.com/p/tts8/1809/77/a19f32eacb75fc02.jpg_304x201_045507ba.jpg',
				title: '杭州西湖游船',
				desc: '听南屏晚钟，眺望西湖，倾听白娘子与许仙的传奇爱情故事'
			}, {
				id: '0002',
				imgUrl: 'https://imgs.qunarzz.com/p/tts5/1605/ec/ab66ab8c5d6d52f7.jpg_304x201_20551507.jpg',
				title: '美丽千岛湖',
				desc: '千岛湖,群山连绵林海叠翠,山风徐来松涛呼啸,登山顶而远眺千峰竞秀万壑滴翠,高峡'
			}, {			
				id: '0003',				
				imgUrl: 'https://imgs.qunarzz.com/p/tts2/1805/93/5b05772eec280402.jpg_304x201_e2fe8192.jpg',
				title: '江南古镇中的佼佼者乌镇西栅',
				desc: '以河成街，桥街相连，依河筑屋，穿竹石栏，临河水阁，古色古香，是江南典型的"小桥、流水、人家"'
			}]
		}		
	}
}
</script>

<style lang="stylus" scoped>
	@import '~styles/mixins.styl'
	
	.title 
		margin-top: .2rem
		line-height: .8rem
		background: #eee
		text-indent: .2rem
	.item-img-wrapper
		height: 0
		overflow: hidden
		padding-bottom: 33.9%
		.item-img 
			width: 100%
	.item-info
		padding: .1rem
		.item-title
			line-height: .54rem
			font-size: .32rem
			ellipsis()
		.item-desc
			line-height: .4rem
			color: #ccc
			ellipsis()
</style>