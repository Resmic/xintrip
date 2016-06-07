# xintrip
仿翁天信网站旅行足迹
先上截图：
![image](https://raw.githubusercontent.com/Resmic/xintrip/master/screenshot/xintrip.png)

index.html
/*引入src文件夹下资源文件*/
<link rel="stylesheet" media="all" href="./src/jquery-jvectormap.css">
		<script src="./src/jquery-1.8.2.js"></script>
		<style type="text/css" adt="123"></style>
		<script src="./src/jquery-jvectormap.js"></script>
		<script src="./src/jquery-mousewheel.js"></script>

		<script src="./src/jvectormap.js"></script>

		<script src="./src/abstract-element.js"></script>
		<script src="./src/abstract-canvas-element.js"></script>
		<script src="./src/abstract-shape-element.js"></script>

		<script src="./src/svg-element.js"></script>
		<script src="./src/svg-group-element.js"></script>
		<script src="./src/svg-canvas-element.js"></script>
		<script src="./src/svg-shape-element.js"></script>
		<script src="./src/svg-path-element.js"></script>
		<script src="./src/svg-circle-element.js"></script>
		<script src="./src/svg-image-element.js"></script>
		<script src="./src/svg-text-element.js"></script>

		<script src="./src/vml-element.js"></script>
		<script src="./src/vml-group-element.js"></script>
		<script src="./src/vml-canvas-element.js"></script>
		<script src="./src/vml-shape-element.js"></script>
		<script src="./src/vml-path-element.js"></script>
		<script src="./src/vml-circle-element.js"></script>
		<script src="./src/vml-image-element.js"></script>

		<script src="./src/map-object.js"></script>
		<script src="./src/region.js"></script>
		<script src="./src/marker.js"></script>

		<script src="./src/vector-canvas.js"></script>
		<script src="./src/simple-scale.js"></script>
		<script src="./src/ordinal-scale.js"></script>
		<script src="./src/numeric-scale.js"></script>
		<script src="./src/color-scale.js"></script>
		<script src="./src/legend.js"></script>
		<script src="./src/data-series.js"></script>
		<script src="./src/proj.js"></script>
		<script src="./src/map.js"></script>


		<script src="./src/jquery-jvectormap-cn-mill-en.js"></script>  //中国地图数据
		
		
		/*
		创建地图，添加图标及图标样式
		*/
		
		$(function() {
				var markers = [{
						latLng: [30.490, 106.040],
						name: '四川 · 南充 - 人生的起点 - 5/1995'
					}, {
						latLng: [22.170, 113.340],
						name: '广东 · 珠海 - 第一个到达的城市 - 12/2005'
					}, {
						latLng: [34.170, 108.570],
						name: '陕西 · 西安 - 第一次长途旅行 - 7/2008'
					}, {
						latLng: [34.300, 109.300],
						name: '陕西 · 渭南 - 去过不一定熟悉 - 8/2011'
					}, {
						latLng: [33.040, 107.010],
						name: '陕西 · 汉中 - 很熟悉的一个陌生的地方 - 6/2011'
					}, {
						latLng: [34.220, 107.090],
						name: '陕西 · 宝鸡 - 感触比较深的地方 - 8/2012'
					}, {
						latLng: [29.350, 106.330],
						name: '中国 · 重庆 - 去过次数最多的地方 - 8/2013'
					}, {
						latLng: [22.480, 108.190],
						name: '广西 · 南宁 - 人生的第二个省会城市 - 8/2013'
					}, {
						latLng: [21.280, 109.070],
						name: '广西 · 北海 - 大学母校的所在地 - 8/2013'
					}, {
						latLng: [30.400, 104.040],
						name: '四川 · 成都 - 算是缘分吧 - 2/2014'
					}, {
						latLng: [22.380, 110.090],
						name: '广西 · 玉林 - 第一次公费“出游” - 4/2014'
					}, {
						latLng: [39.550, 116.240],
						name: '中国 · 北京 - 算“北漂”？ - 6/2014'
					}, {
						latLng: [34.200, 108.430],
						name: '陕西 · 咸阳 - 单纯的路过 - 8/2014'
					}, {
						latLng: [23.190, 109.240],
						name: '广西 · 柳州 - 还是公费“出游” - 4/2015'
					}, {
						latLng: [23.080, 113.140],
						name: '广东 · 广州 - 逐梦的地方 - 7/2015'
					}, {
						latLng: [31.360, 105.580],
						name: '四川 · 阆中 - 作为南部的后花园 - 2/2016'
					}, {
						latLng: [22.330, 114.070],
						name: '广东 · 深圳 - 人生第一次自费旅行 - 5/2016'
					}, ],
					values1 = [408, 512, 550, 781],
					values2 = [1, 2, 3, 4],
					values3 = {
						'4': 'bank',
					};
				$('#map1').vectorMap({
					map: 'cn_mill_en',
					panOnDrag: false,
					backgroundColor: '#A8B2CB',
					markers: markers,
					markerStyle: {
						initial: {
							fill: '#FF444E',
							stroke: '#FF444E',
							"fill-opacity": 1,
							"stroke-width": 1,
							"stroke-opacity": 1,
							r: 4
						},
						hover: {
							stroke: 'black',
							"stroke-width": 2,
							cursor: 'pointer'
						},
						selected: {
							fill: 'blue'
						},
						selectedHover: {}
					},
					labels: {
						render: function(code) {
							var doNotShow = ['US-RI', 'US-DC'];
							if (doNotShow.indexOf(code) === -1) {
								return code.split('-')[1];
							}
						},
					}
				});
				
				
				详细请参考源码！
