<template>
	<div class="video-detail">
		<div class="video-div mt20">
			<p class="c_blue"><router-link to="/supervise/parkSecurity">返回</router-link></p>
			<video :src="videoIp+'v5.mp4'" controls="controls" :width="videoWidth" :height="videoHeight"></video>
  	</div>
  	<div class="video-right">
  		<p>云台控制</p>
  		<div class="video-right-top">
  			<div class="video-controls"></div>
  			<div class="mt20">
			    <span class="demonstration fl">巡航速度</span>
			    <el-slider v-model="value1"></el-slider>
			  </div>
			  <div class="mt20">
			    <span class="demonstration fl">焦距调节</span>
			    <el-slider v-model="value2"></el-slider>
			  </div>
  		</div>
  		<div class="video-right-bottom">
  			<div class="views-title views-title-a">
	    		<ul class="clearfix">
	    			<li>
           	 	<a>预置点设置</a>
	    			</li>
	    			<li class="active">
           	 	<a>巡航路径设置</a>
	    			</li>
	    		</ul>
	    	</div>
	    	<div class="video-settings">
	    		<ul>
	    			<li>预置点</li>
	    			<li>速度</li>
	    			<li>时间（s）</li>
	    		</ul>
	    		<ul>
	    			<li><el-input v-model="input"></el-input></li>
	    			<li><el-input v-model="input"></el-input></li>
	    			<li><el-input v-model="input"></el-input></li>
	    		</ul>
	    		<ul>
	    			<li><el-input v-model="input"></el-input></li>
	    			<li><el-input v-model="input"></el-input></li>
	    			<li><el-input v-model="input"></el-input></li>
	    		</ul>
	    	</div>
  		</div>
  	</div>
	</div>
</template>
<style lang="scss" scoped>
  .video-detail{
  	width: 100%;
    .video-div{
    	float: left;
    	width: 620px;
    	margin-left: 10%;
    	p{
				margin-bottom: -5px;
    	}
    }
    .video-right{
    	float: right;
    	width: 30%;
    	margin-top:20px;
    	.video-right-top{
    		width:100%;
    		background: #f7f7f7;
    		padding: 30px;
    		.video-controls{
    			width: 148px;
    			height: 148px;
    			margin:0 auto;
    			background: url('../../assets/images/supervise/arrows_act.png');
    		}
    		.el-slider{ margin-left: 85px;}
    	}
    	.video-right-bottom{
    		.video-settings{
    			width: 100%;
    			background: #f7f7f7;
    			height: 300px;
    			padding-top: 20px;
    			ul{
    				overflow: hidden;
    				li{
    					width: 24%;
    					text-align: center;
    					float: left;
    					margin-left: 20px;
    					.el-input{ 
    						width: 100%;
    						
    					}
    				}
    			}
    		}
    	}
    }
  }
</style>
<script>
  export default{
    data(){
      return{
      	input:'',
        videoWidth: 600,
        videoHeight: 370,
        videoIp: 'http://192.168.49.10:82/video/',
        value1: 30,
        value2: 50,
      }
    }
  }
</script>