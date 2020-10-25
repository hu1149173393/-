<template>
    <div class="A_homepage">
        <div id="container"></div>
        <div id="container2"></div>
    </div>
</template>

<script>
export default {
    name:'A_homepage',
    data(){
        return {

        }
    },
    mounted () {
        this.drawLine();
        this.drawLine2();
    },
    methods:{
        drawLine () {
        var chart = Highcharts.chart('container', {
            chart: {
                type: 'bar'
            },
            title: {
                text: '各洲不同时间的人口条形图'
            },
            subtitle: {
                text: '慢慢学习'
            },
            xAxis: {
                categories: ['非洲', '美洲', '亚洲', '欧洲', '大洋洲'],
                title: {
                    text: null
                }
            },
            yAxis: {
                min: 0,
                title: {
                    text: '人口总量 (百万)',
                    align: 'high'
                },
                labels: {
                    overflow: 'justify'
                }
            },
            tooltip: {
                valueSuffix: ' 百万'
            },
            plotOptions: {
                bar: {
                    dataLabels: {
                        enabled: true,
                        allowOverlap: true // 允许数据标签重叠
                    }
                }
            },
            legend: {
                layout: 'vertical',
                align: 'right',
                verticalAlign: 'top',
                x: -40,
                y: 100,
                floating: true,
                borderWidth: 1,
                backgroundColor: ((Highcharts.theme && Highcharts.theme.legendBackgroundColor) || '#FFFFFF'),
                shadow: true
            },
            series: [{
                name: '1800 年',
                data: [107, 31, 635, 203, 2]
            }, {
                name: '1900 年',
                data: [133, 156, 947, 408, 6]
            }, {
                name: '2008 年',
                data: [973, 914, 4054, 732, 34]
            }]
            }); 
        },
        drawLine2(){
            Highcharts.getOptions().colors = Highcharts.map(Highcharts.getOptions().colors, function (color) {
                return {
                    radialGradient: { cx: 0.5, cy: 0.3, r: 0.7 },
                    stops: [
                        [0, color],
                        [1, Highcharts.Color(color).brighten(-0.3).get('rgb')] // darken
                    ]
                };
            });
            // 构建图表
            var chart = Highcharts.chart('container2',{
                title: {
                    text: '2014年某网站各浏览器的访问量占比'
                },
                tooltip: {
                    pointFormat: '{series.name}: <b>{point.percentage:.1f}%</b>'
                },
                plotOptions: {
                    pie: {
                        allowPointSelect: true,
                        cursor: 'pointer',
                        dataLabels: {
                            enabled: true,
                            format: '<b>{point.name}</b>: {point.percentage:.1f} %',
                            style: {
                                color: (Highcharts.theme && Highcharts.theme.contrastTextColor) || 'black'
                            },
                            connectorColor: 'silver'
                        }
                    }
                },
                series: [{
                    type: 'pie',
                    name: '浏览器占比',
                    data: [
                        ['Firefox',   45.0],
                        ['IE',       26.8],
                        {
                            name: 'Chrome',
                            y: 12.8,
                            sliced: true,
                            selected: true
                        },
                        ['Safari',    8.5],
                        ['Opera',     6.2],
                        ['其他',   0.7]
                    ]
                }]
            });
        },
    }

}
</script>

<style>
.A_homepage{
    width: 100%;
    height: 100%;
    /* border: 1px solid red; */
    position: relative;
    top: 0px;
    left: 0px;
    display: flex;
    justify-content: space-around;
}
#container{
    width: 400px;
    height: 300px;
}
#container2{
    width: 400px;
    height: 300px;
}
</style>