<canvas id="demo" width="500" height="260" style="{{background:'red'}}">您的浏览器不支持Canvas</canvas>
<script type="text/javascript">
function funload()
{
	var ctx = document.getElementById("demo").getContext("2d");
	ctx.fillStyle = "#B4C2E5";//background
	ctx.fillRect(0,0,500,180);
	ctx.fillStyle = "#C5E7FF";
	ctx.fillRect(0,180,500,80);
	ctx.beginPath();//background lines
	ctx.lineWidth = 2;
	ctx.strokeStyle = "#7E8DAE";
	ctx.moveTo(28,0);
	ctx.lineTo(28,35);
	ctx.lineTo(0,35);
	ctx.moveTo(99,24);
	ctx.lineTo(99,53);
	ctx.lineTo(140,53);
	ctx.moveTo(156,16);
	ctx.lineTo(181,16);
	ctx.moveTo(350,0);
	ctx.lineTo(350,21);
	ctx.moveTo(373,0);
	ctx.lineTo(373,12);
	ctx.moveTo(500,24);
	ctx.lineTo(419,24);
	ctx.lineTo(419,152);
	ctx.lineTo(400,152);
	ctx.moveTo(468,55);
	ctx.lineTo(486,55);
	ctx.lineTo(486,38);
	ctx.lineTo(449,38);
	ctx.lineTo(449,55);
	ctx.lineTo(468,55);
	ctx.lineTo(468,67);
	ctx.lineTo(449,67);
	ctx.lineTo(449,84);
	ctx.lineTo(486,84);
	ctx.lineTo(486,67);
	ctx.lineTo(468,67);
	ctx.moveTo(500,180);
	ctx.lineTo(390,180);
	ctx.moveTo(0,180);
	ctx.lineTo(130,180);
	ctx.moveTo(0,147);
	ctx.lineTo(117,147);
	ctx.stroke();
	ctx.beginPath();
	ctx.strokeStyle = "#B3D5EE";
	ctx.moveTo(0,186);
	ctx.lineTo(125,186);
	ctx.moveTo(0,196);
	ctx.lineTo(37,196);
	ctx.lineTo(42,190);
	ctx.lineTo(82,190);
	ctx.lineTo(67,205);
	ctx.lineTo(27,205);
	ctx.lineTo(37,196);
	ctx.moveTo(76,196);
	ctx.lineTo(139,196);
	ctx.moveTo(35,205);
	ctx.lineTo(22,214);
	ctx.lineTo(0,219);
	ctx.moveTo(46,205);
	ctx.lineTo(8,235);
	ctx.moveTo(54,205);
	ctx.lineTo(47,214);
	ctx.lineTo(58,221);
	ctx.lineTo(44,235);
	ctx.moveTo(0,235);
	ctx.lineTo(178,235);
	ctx.moveTo(0,250);
	ctx.lineTo(171,250);
	ctx.moveTo(500,186);
	ctx.lineTo(384,186);
	ctx.moveTo(469,186);
	ctx.lineTo(487,197);
	ctx.lineTo(470,197);
	ctx.lineTo(500,213);
	ctx.moveTo(470,197);
	ctx.lineTo(449,197);
	ctx.lineTo(458,203);
	ctx.lineTo(448,204);
	ctx.lineTo(461,212);
	ctx.lineTo(500,224);
	ctx.moveTo(449,197);
	ctx.lineTo(439,190);
	ctx.lineTo(400,190);
	ctx.lineTo(409,197);
	ctx.lineTo(379,197);
	ctx.moveTo(409,197);
	ctx.lineTo(416,203);
	ctx.lineTo(458,203);
	ctx.moveTo(429,203);
	ctx.lineTo(439,212);
	ctx.lineTo(432,221);
	ctx.lineTo(446,235);
	ctx.moveTo(442,203);
	ctx.lineTo(482,235);
	ctx.moveTo(500,235);
	ctx.lineTo(340,235);
	ctx.moveTo(355,236);
	ctx.lineTo(370,260);
	ctx.stroke();
	ctx.beginPath();//head
	ctx.fillStyle = "#fff";
	ctx.strokeStyle = "#826E56";
	ctx.moveTo(328,210);
	ctx.quadraticCurveTo(295,226,260,225);
	ctx.quadraticCurveTo(221,226,188,210);
	ctx.quadraticCurveTo(186,213,181,212);
	ctx.quadraticCurveTo(158,220,155,200);
	ctx.quadraticCurveTo(138,202,137,183);
	ctx.quadraticCurveTo(122,178,127,161);
	ctx.quadraticCurveTo(113,146,123,131);
	ctx.quadraticCurveTo(116,114,125,103);
	ctx.quadraticCurveTo(116,86,133,74);
	ctx.quadraticCurveTo(127,55,150,53);
	ctx.quadraticCurveTo(150,29,176,29);
	ctx.quadraticCurveTo(179,11,198,16);
	ctx.quadraticCurveTo(212,-3,231,6);
	ctx.quadraticCurveTo(240,-4,258,6);
	ctx.quadraticCurveTo(276,-3,287,5);
	ctx.quadraticCurveTo(307,-4,319,17);
	ctx.quadraticCurveTo(339,10,343,31);
	ctx.quadraticCurveTo(368,30,369,52);
	ctx.quadraticCurveTo(392,57,387,75);
	ctx.quadraticCurveTo(401,90,393,105);
	ctx.quadraticCurveTo(403,117,395,130);
	ctx.quadraticCurveTo(406,148,392,161);
	ctx.quadraticCurveTo(395,180,378,187);
	ctx.quadraticCurveTo(378,203,363,206);
	ctx.quadraticCurveTo(355,221,337,213);
	ctx.quadraticCurveTo(331,213,328,210);
	ctx.moveTo(318,215);//body
	ctx.quadraticCurveTo(319,221,318,226);
	ctx.quadraticCurveTo(326,233,322,241);
	ctx.quadraticCurveTo(330,249,328,260);
	ctx.lineTo(187,260);
	ctx.lineTo(193,232);
	ctx.quadraticCurveTo(195,225,201,220);
	ctx.quadraticCurveTo(200,216,200,214);	
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();//face
	ctx.fillStyle = "#FFDEB1";
	ctx.strokeStyle = "#826E56";
	ctx.moveTo(328,210);
	ctx.quadraticCurveTo(295,226,260,225);
	ctx.quadraticCurveTo(221,226,188,210);
	ctx.quadraticCurveTo(192,203,189,196);
	ctx.quadraticCurveTo(198,182,183,176);
	ctx.quadraticCurveTo(186,162,171,158);
	ctx.quadraticCurveTo(173,150,167,147);
	ctx.quadraticCurveTo(175,134,169,122);
	ctx.quadraticCurveTo(174,113,174,101);
	ctx.quadraticCurveTo(186,98,188,84);
	ctx.quadraticCurveTo(203,86,213,76);
	ctx.quadraticCurveTo(219,78,224,80);
	ctx.bezierCurveTo(237,97,279,96,295,77);
	ctx.quadraticCurveTo(300,76,305,76);
	ctx.quadraticCurveTo(312,89,329,91);
	ctx.quadraticCurveTo(330,105,343,111);
	ctx.quadraticCurveTo(339,126,352,134);
	ctx.quadraticCurveTo(344,146,346,161);
	ctx.quadraticCurveTo(331,163,334,179);
	ctx.quadraticCurveTo(322,185,331,199);
	ctx.quadraticCurveTo(326,205,328,210);
	ctx.moveTo(133,74);//ear
	ctx.bezierCurveTo(120,80,117,98,103,103);
	ctx.quadraticCurveTo(110,112,121,111);
	ctx.quadraticCurveTo(122,107,125,103);
	ctx.quadraticCurveTo(116,86,133,74);
	ctx.moveTo(387,75);
	ctx.bezierCurveTo(405,80,402,98,419,103);
	ctx.quadraticCurveTo(409,112,397,111);
	ctx.quadraticCurveTo(395,105,393,105);
	ctx.quadraticCurveTo(401,90,387,75);
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();//arm
	ctx.fillStyle = "#FFDEB1";
	ctx.strokeStyle = "#826E56";
	ctx.moveTo(200,214);
	ctx.quadraticCurveTo(182,227,174,242);
	ctx.quadraticCurveTo(166,255,177,260);
	ctx.quadraticCurveTo(198,254,211,246);
	ctx.quadraticCurveTo(217,247,222,241);
	ctx.quadraticCurveTo(217,247,218,244);
	ctx.quadraticCurveTo(225,253,230,241);
	ctx.quadraticCurveTo(229,236,222,236);
	ctx.quadraticCurveTo(229,236,230,241);
	ctx.quadraticCurveTo(235,232,223,229);
	ctx.quadraticCurveTo(228,229,231,227);
	ctx.moveTo(231,233);
	ctx.quadraticCurveTo(239,218,216,218);
	ctx.quadraticCurveTo(222,220,222,218);
	ctx.bezierCurveTo(219,206,208,220,202,231);
	ctx.quadraticCurveTo(188,235,174,243);
	ctx.quadraticCurveTo(183,238,194,232);
	ctx.quadraticCurveTo(194,224,201,220);
	ctx.lineTo(200,214);
	ctx.moveTo(318,215);
	ctx.quadraticCurveTo(319,221,318,226);
	ctx.quadraticCurveTo(326,233,322,241);
	ctx.quadraticCurveTo(330,249,328,260);
	ctx.lineTo(343,260);
	ctx.bezierCurveTo(350,247,343,237,318,215);
	ctx.moveTo(327,249);
	ctx.lineTo(331,245);
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();//horn
	ctx.fillStyle = "#7F5D42";
	ctx.strokeStyle = "#38332F";
	ctx.moveTo(144,53);
	ctx.bezierCurveTo(128,32,100,19,92,20);
	ctx.quadraticCurveTo(89,18,95,13);
	ctx.bezierCurveTo(115,6,147,8,176,26);
	ctx.quadraticCurveTo(175,29,176,29);
	ctx.quadraticCurveTo(150,30,150,52);
	ctx.quadraticCurveTo(144,53,145,54);
	ctx.moveTo(111,27);
	ctx.quadraticCurveTo(106,15,116,10);
	ctx.moveTo(129,37);
	ctx.quadraticCurveTo(129,20,146,13);
	ctx.moveTo(143,51);
	ctx.quadraticCurveTo(154,34,172,24);
	ctx.moveTo(376,54);
	ctx.bezierCurveTo(386,35,399,25,427,21);
	ctx.quadraticCurveTo(432,18,425,14);
	ctx.bezierCurveTo(408,6,388,6,343,27);
	ctx.quadraticCurveTo(343,28,344,31);
	ctx.quadraticCurveTo(367,32,369,51);
	ctx.quadraticCurveTo(371,53,376,54);
	ctx.moveTo(377,51);
	ctx.quadraticCurveTo(366,34,349,24);
	ctx.moveTo(391,36);
	ctx.quadraticCurveTo(388,20,378,12);
	ctx.moveTo(410,24);
	ctx.quadraticCurveTo(411,14,404,10);
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();//eyes and nose
	ctx.fillStyle = "#fff";
	ctx.strokeStyle = "#826E56";
	ctx.arc(213,133,22,0,Math.PI*2,true);
	ctx.moveTo(325,133);
	ctx.arc(303,133,22,0,Math.PI*2,true);
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();
	ctx.fillStyle = "#000";
	ctx.arc(213,136,10,0,Math.PI*2,true);
	ctx.moveTo(311,136);
	ctx.arc(302,136,10,0,Math.PI*2,true);
	ctx.moveTo(259,181);
	ctx.bezierCurveTo(282,181,282,162,259,162);
	ctx.bezierCurveTo(236,162,236,181,259,181);
	ctx.fill();
	ctx.beginPath();
	ctx.fillStyle = "#fff";
	ctx.arc(208,132,2,0,Math.PI*2,true);
	ctx.moveTo(298,132);
	ctx.arc(296,132,2,0,Math.PI*2,true);
	ctx.moveTo(248,171);
	ctx.bezierCurveTo(254,171,254,166,248,166);
	ctx.bezierCurveTo(242,166,242,171,248,171);
	ctx.fill();
	ctx.beginPath();//eyebrows
	ctx.fillStyle = "#46403B";
	ctx.moveTo(196,102);
	ctx.quadraticCurveTo(218,96,236,110);
	ctx.quadraticCurveTo(221,86,196,102);
	ctx.moveTo(279,109);
	ctx.quadraticCurveTo(297,94,320,100);
	ctx.quadraticCurveTo(295,84,279,109);
	ctx.fill();//mouth
	ctx.beginPath();
	ctx.fillStyle = "#A5422B";
	ctx.strokeStyle = "#88381D";
	ctx.moveTo(280,209);
	ctx.bezierCurveTo(280,195,239,195,239,210);
	ctx.bezierCurveTo(236,216,285,217,280,209);
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();
	ctx.fillStyle = "#F6846C";
	ctx.moveTo(280,209);
	ctx.bezierCurveTo(279,204,240,204,239,210);
	ctx.bezierCurveTo(236,216,285,217,280,209);
	ctx.fill();
	ctx.beginPath();//neck
	ctx.fillStyle = "#294473";
	ctx.strokeStyle = "#294473";
	ctx.moveTo(318,216);
	ctx.quadraticCurveTo(265,229,233,224);
	ctx.quadraticCurveTo(233,229,232,232);
	ctx.quadraticCurveTo(282,238,318,215);
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();//button
	ctx.fillStyle = "#FAC55D";
	ctx.strokeStyle = "#413609";
	ctx.arc(260,242,15,0,Math.PI*2,true);
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();
	ctx.fillStyle = "#000";
	ctx.strokeStyle = "#413609";
	ctx.arc(261,243,4,0,Math.PI*2,true);
	ctx.moveTo(261,243);
	ctx.lineTo(265,255);
	ctx.fill();
	ctx.stroke();
	ctx.beginPath();//add
	ctx.strokeStyle = "#826E56";
	ctx.moveTo(232,49);
	ctx.quadraticCurveTo(212,62,225,81);
	ctx.moveTo(295,76);
	ctx.quadraticCurveTo(299,63,288,60);
	ctx.quadraticCurveTo(297,67,287,67);
	ctx.quadraticCurveTo(278,70,273,50);
	ctx.stroke();
}
funload();
</script>
- 👋 Hi, I'm @MygengBin. I'm a boy.

- 👀 I'm interested in Code, front-end and back-end.

- 🌱 I'm currently learning Java Script, Next want to Study Open Soure frame. next ready Contribute code to open source projects

- 💞️ I'm looking to collaborate on None.

- 📫 How to reach me Java script. learing...

- [Nginx CORS](./nginx跨域/README.md)

- [Front end Check System Theme](./markdown/%E5%89%8D%E7%AB%AF%E5%88%A4%E6%96%AD%E7%B3%BB%E7%BB%9F%E4%B8%BB%E9%A2%98.md)

- [Java script check current language](./markdown/JS判断当前系统语言、浏览器语言.md)

- [隐藏electron窗体菜单栏的几种方式](./markdown/隐藏electron窗体菜单栏的几种方式.md)

- [解决php的URLencode编码时将空格转成+的问题](./markdown/%E8%A7%A3%E5%86%B3php%E7%9A%84URLencode%E7%BC%96%E7%A0%81%E6%97%B6%E5%B0%86%E7%A9%BA%E6%A0%BC%E8%BD%AC%E6%88%90%2B%E7%9A%84%E9%97%AE%E9%A2%98.md)

- [MySQL8.0 创建nodejs支持的用户](./markdown/MySQL8.0_create_a_nodejs_support_user.md)

- [PHP json_encode无输出问题以及处理调试方案](./markdown/PHP%20json_encode%E6%97%A0%E8%BE%93%E5%87%BA%E9%97%AE%E9%A2%98%E4%BB%A5%E5%8F%8A%E5%A4%84%E7%90%86%E8%B0%83%E8%AF%95%E6%96%B9%E6%A1%88.md)

- [PHP上传文件失败总结](./markdown/PHP%E4%B8%8A%E4%BC%A0%E6%96%87%E4%BB%B6%E5%A4%B1%E8%B4%A5%E6%80%BB%E7%BB%93.md)

- Git 当前分支提交到其他分支
```cmd
git.exe push --progress "origin" develop:master
```  
<!---
  MygengBin/MygengBin is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
  You can click the Preview link to take a look at your changes.
  --->
