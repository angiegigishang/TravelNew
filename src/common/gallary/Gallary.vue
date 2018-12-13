<template>
	<div class="container">
		<div class="wrapper">
			<swiper :options="swiperOptions">
		    <!-- slides -->
			    <swiper-slide>
			    	<img class="gallary-img" src="https://img1.qunarzz.com/des-mis/ad/1809/40/bf8ee7f716f9b2.jpg"/>
			    </swiper-slide>
			    <swiper-slide>
			    	<img class="gallary-img" src="https://img1.qunarzz.com/des-mis/ad/1809/40/bf8ee7f716f9b2.jpg"/>
			    </swiper-slide>
			    <!-- Optional controls -->
			    <div class="swiper-pagination"  slot="pagination"></div>
			</swiper>
		</div>
	</div>
</template>

<script>
export default {
	name: 'CommonGallary',
	/*props: {
		imgs: {
			type: Array,
			default () {
				return ['https://img1.qunarzz.com/des-mis/ad/1809/40/bf8ee7f716f9b2.jpg', 'https://img1.qunarzz.com/des-mis/ad/1809/40/bf8ee7f716f9b2.jpg']
			}
		}
	},*/
	data () {
		return{
			swiperOptions: {
				pagination: '.swiper-pagination',
				paginationType: 'fraction'
			}
		}
	}
}
</script>

<style lang="stylus" scoped>
	.container >>> .swiper-container
		overflow: inherit
		
	.container
		display: flex
		flex-direction: column
		justify-content: center
		z-index: 99
		position: fixed
		left: 0
		right: 0
		top: 0
		bottom: 0
		background: #000
		.wrapper 
			height: 0
			width: 100%
			padding-bottom: 100%
			.gallary-img
				width: 100%
			.swiper-pagination
				color: #fff
				bottom: -.5rem
</style>