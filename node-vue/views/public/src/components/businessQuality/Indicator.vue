<template>
<div class="indicator">
    <div class="every"><p>质量优良率</p></div>
    <div class="every"><p>直播切换优良率</p></div>
    <div class="every"><p>点播加载优良率</p></div>
    <div class="every"><p>优良用户数</p></div>
    <div class="every"><p>播放用户数</p></div>
    <div class="every"><p>告警数</p></div>
</div>
</template>

<script>
</script>

<style>
.indicator{
    width:100%;
    height:60px;
    line-height:60px;
    display: flex;
    justify-content:space-around;
    margin:20px 0px;
}
.indicator .every{
    width:12%;
    border:1px solid #00ffff;
    border-radius:3px;
    color:#00ffff;
    padding:0px 10px;
    font-size:14px;
}
.indicator .every p{
    width:90%;
    height:100%;
    margin-left:5%
}
</style>