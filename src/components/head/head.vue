<template>
  <div class="header">
    <div class="wrapper">
      <div class="avatar">
         <img width="64" height="64" :src="seller.avatar" alt="">
      </div>
      <div class="content">
        <div class="title">
          <span class="brand"></span>
          <span class="name">{{seller.name}}</span>
        </div>
        <div class="desc">
          {{seller.description}}/{{seller.deliveryTime}}分钟送达
        </div>
        <div v-if="seller.supports" class="suppert">
          <span class="icon"></span>
          <span class="text"> {{seller.supports[0].description}}</span>
        </div>
      </div>
	  <div class="supprt-count" v-if="seller.supports">
		  <span class="count">{{seller.supports.length}}个</span>
		  <i class="">></i>
	  </div>
    </div>
  </div>
</template>

<script>
export default {
    name:"Header",
    props:["seller"],
    
    data(){
      return{

      }
    }
}

</script>

<style scoped lang="stylus">
.header 
	background-color #eee
	.wrapper
		padding .12rem
		font-size 0
		position relative
		.avatar
			display inline-block
			vertical-align top
			img 
				border-radius .04rem
		.content
			display inline-block
			font-size .14rem
			line-height .2rem
			margin-left .2rem
			.title
				font-size .16rem
				color red
				.brand
					display inline-block 
					width 30px
					height 18px
					background-image url("../../common/img/brand@2x.png")
					vertical-align middle
					background-repeat no-repeat
					background-size 30px 18px
					margin-left .06rem

				.name
					margin-left .04rem
					vertical-align top
					// font-size .16rem
					font-weight bold
			.desc
				line-height .3rem
				margin-left .06rem
			.suppert
				margin-left .04rem
				.icon	
					display inline-block
					width 16px
					height 16px
					background-image url("../../common/img/decrease_1@2x.png")	
					background-size 16px 16px 
					background-repeat no-repeat
					vertical-align middle


		.supprt-count
			position absolute
			bottom  .1rem
			right .2rem
			width .5rem
			height .26rem
			line-height .26rem
			background-color #999
			color white
			font-size 16px
			text-align center
			border-radius .4rem
			



</style>