<template>
  <div class="wrapper">
	  <swiper :options="swiperOption">
	    <!-- slides -->
	    <swiper-slide v-for="item of swiperList" :key="item.id">
	    	<img class="swiper-img" :src="item.imgUrl"/>
	    </swiper-slide>
	    <!-- Optional controls -->
	    <div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
	</div>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		data () {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
					loop: true
				},
				swiperList: [{
					id: '0001',
					imgUrl:'http://img1.qunarzz.com/vc/ce/4b/45/7f78e2003fb5fb65c57eb1a800.jpg'
				}, {
					id: '002',
					imgUrl:'http://img1.qunarzz.com/vc/f3/ea/ae/095dd61c09f2797ba9147bd03f.jpg'
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
		background: #fff !important
	    .wrapper{
	    	overflow: hidden
	    	width: 100%
	    	height: 0
	    	padding-bottom: 31.25%
			.swiper-img{
				width: 100%
				}
			}
</style>