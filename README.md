# html<!DOCTYPE html>
<html>

	<head>
		<meta charset="utf-8" />
		<title></title>
		<style type="text/css">
			* {
				margin: 0;
				padding: 0;
			}
			
			.wrap-box {
				width: 100%;
				height: auto;
				perspective: 800px;
				margin-top: 200px;
			}
			
			.box-content {
				width: 200px;
				height: 200px;
				margin: 2em auto 10em;
				transform-style: preserve-3d;
				-kebkit-transform-style: preserve-3d;
				position: relative;
				animation: rotate 10s infinite linear;
			}
			
			@keyframes rotate {
				0% {
					transform: rotateX(-10deg) rotateY(0deg);
				}
				50% {
					transform: rotateX(-10deg) rotateY(180deg);
				}
				100% {
					transform: rotateX(-10deg) rotateY(360deg);
				}
			}
			
			@-webkit-keyframes rotate {
				0% {
					transform: rotateX(-10deg) rotateY(0deg);
				}
				50% {
					transform: rotateX(-10deg) rotateY(180deg);
				}
				100% {
					transform: rotateX(-10deg) rotateY(360deg);
				}
			}
			
			.box-content img {
				width: 100%;
			}
			
			.box-content div {
				position: absolute;
				transition: all 0.2s ease;
			}
			/*
			 外层div
			 */
			
			.box-content div[class^="l"] {
				width: 200px;
				height: 200px;
				top: 0px;
			}
			/*
			 中间div
			 */
			
			.box-content div[class^="m"] {
				width: 150px;
				height: 150px;
				top: 30px;
				opacity: 0;
			}
			/*
			 内层div
			 */
			
			.box-content div[class^="s"] {
				width: 100px;
				height: 100px;
				opacity: 0;
				top: 50px;
			}
			
			.box-content:hover div[class^="l"] {
				top: 0;
			}
			
			.box-content:hover div[class^="m"] {
				opacity: 1;
			}
			
			.box-content:hover div[class^="s"] {
				opacity: 1;
			}
			/*
			 前方元素
			 */
			
			.box-content div[class*="front"] {
				transform: translateZ(100px);
				-webkit-transform: translateZ(100px);
			}
			/*
			 左边元素
			 * */
			
			.box-content div[class*="left"] {
				transform: translateX(-100px) rotateY(-90deg);
				-webkit-transform: translateX(-100px) rotateY(-90deg);
			}
			/*
			 后方元素
			 */
			
			.box-content div[class*="back"] {
				transform: translateZ(-100px);
				-webkit-transform: translateZ(-100px);
			}
			/*
			 右边元素
			 */
			
			.box-content div[class*="right"] {
				transform: translateX(100px) rotateY(90deg);
				-webkit-transform: translateX(100px) rotateY(90deg);
			}
			
			.box-content:hover div.l-front {
				transform: translateZ(250px);
				-webkit-transform: translateZ(250px);
			}
			
			.box-content:hover div.m-front {
				transform: translateZ(150px);
				-webkit-transform: translateZ(150px);
			}
			
			.box-content:hover div.s-front {
				transform: translateZ(50px);
				-webkit-transform: translateZ(50px);
			}
			.box-content:hover div.l-left{
			    transform: translateX(-250px) rotateY(-90deg);
			    -webkit-transform: translateX(-250px) rotateY(-90deg);
			}
			.box-content:hover div.m-left {
				transform: translateX(-150px) rotateY(-90deg);
				-webkit-transform: translateX(-150px) rotateY(-90deg);
			}
			
			.box-content:hover div.s-left {
				transform: translateX(-50px) rotateY(-90deg);
				-webkit-transform: translateX(-50px) rotateY(-90deg);
			}
			
			.box-content:hover div.l-back {
				transform: translateZ(-250px);
				-webkit-transform: translateZ(-250px);
			}
			
			.box-content:hover div.m-back {
				transform: translateZ(-150px);
				-webkit-transform: translateZ(-150px);
			}
			
			.box-content:hover div.s-back {
				transform: translateZ(-50px);
				-webkit-transform: translateZ(-50px);
			}
			
			.box-content:hover div.l-right {
				transform: translateX(250px) rotateY(90deg);
				-webkit-transform: translateX(250px) rotateY(90deg);
			}
			
			.box-content:hover div.m-right {
				transform: translateX(150px) rotateY(90deg);
				-webkit-transform: translateX(150px) rotateY(90deg);
			}
			
			.box-content:hover div.s-right {
				transform: translateX(50px) rotateY(90deg);
				-webkit-transform: translateX(50px) rotateY(90deg);
			}
		</style>
	</head>

	<body>
		<div class="wrap-box">
			<div class="box-content">
				<div class="l-front"><img alt="1" src="img/hot2.gif" /></div>
				<div class="l-left"><img alt="1" src="img/hot4.gif" /></div>
				<div class="l-back"><img alt="1" src="img/hot8.gif" /></div>
				<div class="l-right"><img alt="1" src="img/hot10.gif" /></div>

				<div class="m-front"><img alt="1" src="img/hot5.gif" /></div>
				<div class="m-left"><img alt="1" src="img/hot7.gif" /></div>
				<div class="m=back"><img alt="1" src="img/hot9.gif" /></div>
				<div class="m-right"><img alt="1" src="img/hot11.gif" /></div>

				<div class="s-front"><img alt="1" src="img/hot2.gif" /></div>
				<div class="s-left"><img alt="1" src="img/hot4.gif" /></div>
				<div class="s-back"><img alt="1" src="img/hot8.gif" /></div>
				<div class="s-right"><img alt="1" src="img/hot10.gif" /></div>
			</div>
		</div>
	</body>

</html>
