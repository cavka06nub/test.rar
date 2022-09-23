#  snow
work
*,*:after,*:before{
-webkit-box-sizing:border-box;
-moz-box-sizing:border-box;
-ms-box-sizing:border-box;
box-sizing: border-box;
}

body{
	font-family: arial;
	font-size: 16px;
	margin: 0;
	background: #fff;
	color: #000;

}

.snow_wrap{
	height: 100vh;
	width: 100%;
	
	position: relative;
	background-position:center bottom;
	background: url(../image/imgg.jpg);
	overflow: hidden;
	background-repeat: no-repeat;
	background-size: cover;
}

.snow,.snow:after,.snow:before{
	content: "";
	position: absolute;
	top: -650px;
	left: 0;
	right: 0;
	bottom: 0;
	background-image: 
	radial-gradient(4px 4px at 100px 50px, #fff, transparent),
	radial-gradient(6px 6px at 200px 150px, #fff, transparent),
	radial-gradient(3px 3px at 300px 250px, #fff, transparent),
	radial-gradient(4px 4px at 400px 350px, #fff, transparent),
	radial-gradient(6px 6px at 500px 100px, #fff, transparent),
	radial-gradient(3px 3px at 50px 200px, #fff, transparent),
	radial-gradient(4px 4px at 150px 300px, #fff, transparent),
	radial-gradient(6px 6px at 250px 400px, #fff, transparent),
	radial-gradient(3px 3px at 350px 500px, #fff, transparent);
	background-size: 650px 650px;

	animation:snowAnim 3s linear;
	animation-iteration-count:infinite; 
}
.snow:after{
	margin-left:-250px;
	opacity: 0.5;
	filter:blur(2px);
	animation-direction: reverse;
	animation-duration: 9s;
}

.snow:before{
	margin-left:-350px;
	opacity: 0.7;
	filter:blur(1px);
	animation-direction: reverse;
	animation-duration: 9s;
}

@keyframes snowAnim{
	from{
		transform: translateY(0);
	}
	to{
		transform:  translateY(650px);
	}
}
