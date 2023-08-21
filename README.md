<!DOCTYPE HTML>
<html>
<head>
	<title>Our Love Story</title>
	<meta http-equiv="content-type" content="text/html; charset=UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
	<style type="text/css">
		@font-face {
			font-family: digit;
			src: url('digital.ttf') format("truetype");
		}
	</style>
	<link href="css/default.css" type="text/css" rel="stylesheet">
	<script type="text/javascript" src="js/jquery.js"></script>
	<script type="text/javascript" src="js/garden.js"></script>
	<script type="text/javascript" src="js/functions.js"></script>
</head>

<body>
<div id="mainDiv">
	<div id="content">
		<div id="code">
			<span class="comments">##</span><br/>
			<span class="comments"># I am a programmer,</span><br/>
			<span class="comments"># so I write code to celebrate Valentine's Day in coder's way.</span><br/>
			<span class="comments">##</span><br/>
			i = Boy(<span class="string">"Qingcai Cui"</span>);<br/>
			u = Girl(<span class="string">"Qian Ma"</span>);<br/>
			<span class="comments"># May 1, 2023, I meet you. </span><br/>
			i.meet(u)<br/>
			<span class="comments"># Afterwards, I confessed to you. </span><br/>
			i.confess(u)<br/>
			<span class="comments"># May 20, 2023, You became my girlfriend.</span><br/>
			u.accepted(i)<br/>
			<span class="comments"># Since then, we spent harmony happiness life every day.</span><br/>
			happy(u, i)<br/>
			<span class="comments"># We enjoy studying together.</span><br/>
			study(u, i)<br/>
			<span class="comments"># We enjoy cuisine together.</span><br/>
			dine(u, i)<br/>
			<span class="comments"># We enjoy appointment together.</span><br/>
			appoint(u, i)<br/>
			<span class="comments"># We enjoy vacation together.</span><br/>
			vacation(u, i)<br/>
			<span class="comments"># Sometimes there are a few conflicts between us.</span><br/>
			conflict(u, i, sometimes=<span class="keyword">True</span>)<br/>
			<span class="comments"># But we are getting more and more in harmony together.</span><br/>
			u.in_harmony_with(i) <br/>
			i.in_harmony_with(u) <br/>
			<span class="comments"># You are the greatest love of my life.</span><br/>
			while <span class="keyword">True</span>:<br/>
			<span class="placeholder"></span><span class="keyword">if</span> u.with(i):<br/>
			<span class="placeholder"></span><span class="placeholder"></span>u = everything<br/>
			<span class="placeholder"></span><span class="keyword">else</span>:<br/>
			<span class="placeholder"></span><span class="placeholder"></span>everything = u<br/>
			<span class="comments"># Waiting me marries you, we will be the happiest couple in the world.</span><br/>
			i.marry(u, in_the_future=<span class="keyword">True</span>)<br/>
			i.live_happily_forever_with(u)<br/>
			<span class="comments"># I love you forever.</span><br/>
		</div>
		<div id="loveHeart">
			<canvas id="garden"></canvas>
			<div id="words">
				<div id="messages">
					Qian, I have fallen in love with you for
					<div id="elapseClock"></div>
				</div>
				<div id="loveu">
					Love u forever and ever.<br/>
					<div class="signature">- Zejun Wang | Germey</div>
				</div>
			</div>
		</div>
	</div>
	<div id="copyright">
		Copyright © 2020 <a href='http://cuiqingcai.com'>cuiqingcai.com</a> 2014-2020
	</div>
</div>
<script type="text/javascript">
	var offsetX = $("#loveHeart").width() / 2;
	var offsetY = $("#loveHeart").height() / 2 - 55;
	var together = new Date();
	// 此处月份介于 0 ~ 11 之间。用本地时间表示，如 8 月要用 7 表示。
	together.setFullYear(2018, 10, 5);
	together.setHours(15);
	together.setMinutes(0);
	together.setSeconds(0);
	together.setMilliseconds(0);

	if (!document.createElement('canvas').getContext) {
		var msg = document.createElement("div");
		msg.id = "errorMsg";
		msg.innerHTML = "Your browser doesn't support HTML5!<br/>Recommend use Chrome 14+/IE 9+/Firefox 7+/Safari 4+";
		document.body.appendChild(msg);
		$("#code").css("display", "none")
		$("#copyright").css("position", "absolute");
		$("#copyright").css("bottom", "10px");
		document.execCommand("stop");
	} else {
		setTimeout(function () {
			startHeartAnimation();
		}, 5000);

		timeElapse(together);
		setInterval(function () {
			timeElapse(together);
		}, 500);

		adjustCodePosition();
		$("#code").typewriter();
	}
</script>
</body>
</html>
