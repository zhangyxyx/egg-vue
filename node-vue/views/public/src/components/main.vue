<template>
<div class="main">
    <HeaderM />
    <Menu/>
    <div class="mainM">
        <Indicator />
        <div style="float:left;width:200px;margin-left:10px;">
            <Sort v-bind:msg="['省质差率Top5','line','prov']"/>
            <Sort v-bind:msg="['地市质差率Top5','bar','city']"/>
        </div>
        <Map />
        <div style="float:left;width:200px;margin-right:10px;">
            <Sort v-bind:msg="['近24小时波动','line','Time24']"/>
            <Sort v-bind:msg="['近30天波动','line','Time30']"/>
            <Sort v-bind:msg="['近12个月波动','bar','Time12']"/>
        </div>
    </div>
    
    <div style="clear:both"></div>
</div>
</template>

<script>
import HeaderM from './businessQuality/headerM.vue'//顶部
import Indicator from './businessQuality/Indicator.vue'//标签
import Menu from './businessQuality/menu.vue'//菜单
import Map from './businessQuality/map.vue'//地图
import Sort from './businessQuality/sort.vue'//省质差率排名

//地市排名
//24小时
//30天
//12个月
export default {
    name:'BQmain',
    components:{
        HeaderM,
        Indicator,
        Sort,
        Map,
        Menu,
    },
    mounted:function(){
        this.initWh();
    },
    methods:{
        initWh:function(){
            console.log(this.$)
            var w=this.$$(window).width();
            var h=this.$$(window).height()
            this.$$(".main").width(w)
            this.$$(".main").height(h)
        }
    }
}
</script>

<style>
.main{
    width:100%;
    height:100%;
    background:url(../assets/img/bg.jpg) no-repeat;
    background-size:100% 100%
}
.mainM{
    width:calc(100% - 62px);
    float:left;
    border:1px solid #00ffff;
}
.mainCon{
    width:100%;
}
/*顶部布局*/
.mainB{
    width:100%;
    height:200px;
    display: flex;
    justify-content:space-around;
    margin:20px 0px;
}
</style>