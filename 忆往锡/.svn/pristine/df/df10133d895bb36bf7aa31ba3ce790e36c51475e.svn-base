/*$(document).ready(function(){ */

$(function(){
   /* 题头的包含有什么区别？？？？*/

    apiready = function() {



        /*修改CSS中父框架的高度*/
        $("body").css("height",api.winHeight-20);


        /*分离js*/

        /*var divFunc = document.getElementById("menu");
            divFunc.onclick=function(){ menuOp();}     
            元素少时直接用byid，多的时候可以选择用下面的方式，
            先用bytagname找出所有元素，再放入数组中
        */

     /*   var areaFunc = document.getElementsByTagName("area");
        for (var r = 0; r < areaFunc.length; r++)
        {
            if (areaFunc[r].getAttribute("id")=="mapGu")
            {
                areaFunc[r].onclick=function(){ mapGu();}
            }
        }*/

/*=================================================*/
        if($api.getStorage('gu1')=='1'){
            $("#guStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('chen1')=='1'){
            $("#chenStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('liao1')=='1'){
            $("#liaoStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('lu1')=='1'){
            $("#luStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('qian1')=='1'){
            $("#qianStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('qin1')=='1'){
            $("#qinStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('shu1')=='1'){
            $("#shuStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('wen1')=='1'){
            $("#wenStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('xue1')=='1'){
            $("#xueStr").attr("src","../image/favPic.png");
        }
        if($api.getStorage('zhang1')=='1'){
            $("#zhangStr").attr("src","../image/favPic.png");
        }




        var divFunc = document.getElementsByTagName("div");
        for (var i = 0; i < divFunc.length; i++) 
        {
            if (divFunc[i].getAttribute("id")=="camera")
            {
                divFunc[i].onclick=function(){ camera();}
            }
            if (divFunc[i].getAttribute("id")=="menu") 
            {
                divFunc[i].onclick=function(){ menuOp();}
                /*  蠢死了…………注意!!
                    element.event=function()
                    { 
                        action 
                    }
                */  
            }
            if (divFunc[i].getAttribute("id")=="home") 
            {
                divFunc[i].onclick=function(){
                    returnBgpic();
                    var user1 = document.getElementById("user1");
                    user1.setAttribute("src","../image/user.png");
                    var home1 = document.getElementById("home1");
                    home1.setAttribute("src","../image/home2.png");
                    var map1 = document.getElementById("map1");
                    map1.setAttribute("src","../image/map.png");
                }
            }

            if (divFunc[i].getAttribute("id")=="user") 
            {
                divFunc[i].onclick=function(){ openF();
                    var user2 = document.getElementById("user1");
                    user2.setAttribute("src","../image/user2.png");
                    var home2 = document.getElementById("home1");
                    home2.setAttribute("src","../image/home.png");
                    var map2 = document.getElementById("map1");
                    map2.setAttribute("src","../image/map.png");
                }
            }

            if (divFunc[i].getAttribute("id")=="map") 
            {
                divFunc[i].onclick=function(){ changeBgPic();
                    var user3 = document.getElementById("user1");
                    user3.setAttribute("src","../image/user.png");
                    var home3 = document.getElementById("home1");
                    home3.setAttribute("src","../image/home.png");
                    var map3 = document.getElementById("map1");
                    map3.setAttribute("src","../image/map2.png");
                }
            }

        }





        function  camera(){
            api.getPicture({
                sourceType: 'camera',
                encodingType: 'jpg',
                mediaValue: 'pic',
                destinationType: 'url',
                allowEdit: true,
                quality: 50,
                targetWidth: 100,
                targetHeight: 100,
                saveToPhotoAlbum: false
            }, function( ret, err ){
                if( ret ){
                    alert( JSON.stringify( ret ) );
                    var fs = api.require('fs');
                    fs.moveTo({
                        oldPath: ret.data,
                        newPath: 'fs://YiWangXi'
                    },function( ret, err ){
                        if( ret.status ){
                            /*alert( JSON.stringify( ret ) );*/
                        }else{
                            /*alert( JSON.stringify( err ) );*/
                        }
                    })
                }else{
                    /*alert( JSON.stringify( err ) );*/
                }
            });
        }



        /*介绍窗口函数*/
        function mapOpen(sta,name){
            api.openFrame({
                name:name,
                url:sta,
                rect:{
                    x:0,
                    y:-250,
                    w:api.winWidth,
                    h:api.winHeight+250
                }
            });
        }
        function mapClose(){
            api.openWin({
                name:'menu',
                url:'../html/frame1.html',
                hScrollBarEnabled:false,
                vScrollBarEnabled:false,
                scaleEnabled:true,
                reload:true,
                rect:{
                    x:0,
                    y:0,
                    w:api.winWidth,
                    h:api.winHeight
                }
            });
        }

        /*点击图标打开介绍窗口*/
        var colFunc = document.getElementsByTagName("div");
        for (var c = 0; c < colFunc.length; c++)
        {
            /*if (colFunc[c].getAttribute("class")=="guPic")*/
            if (colFunc[c].getAttribute("class")=="guPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapGu.html","mapGu");  };
            }
            if (colFunc[c].getAttribute("class")=="chenPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapChen.html","mapChen");  };
            }
            if (colFunc[c].getAttribute("class")=="luPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapLu.html","mapLu");  };
            }
            if (colFunc[c].getAttribute("class")=="wenPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapWen.html","mapWen");  };
            }
            if (colFunc[c].getAttribute("class")=="shuPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapShu.html","mapShu");  };
            }
            if (colFunc[c].getAttribute("class")=="qinPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapQin.html","mapQin");  };
            }
            if (colFunc[c].getAttribute("class")=="xuePic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapXue.html","mapXue");  };
            }
            if (colFunc[c].getAttribute("class")=="qianPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapQian.html","mapQian");  };
            }
            if (colFunc[c].getAttribute("class")=="zhangPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapZhang.html","mapZhang");  };
            }
            if (colFunc[c].getAttribute("class")=="liaoPic")
            {
                colFunc[c].onclick=function(){ mapOpen("../html/mapLiao.html","mapLiao");  };
            }




            /*关闭分享窗口*/
            if (colFunc[c].getAttribute("class")=="theShare")
            {
                colFunc[c].onclick=function(){ closeF("../html/share.html","share");  };
            }

        }


        var classFunc = document.getElementsByTagName("img");
        for (var j = 0; j < classFunc.length; j++)
        {
            /*分享图片弹出*/
            if (classFunc[j].getAttribute("id")=="whare")
            {
                classFunc[j].onclick=function() {
                    /*$(".theShare").fadeIn();*/
                    /*alert(1);*/
                    $(".otherShare").animate({
                        height: '+=150px',
                        width: '+=150px',
                        opacity:1
                    },"slow");
                }
            }



            /*两个关闭弹框选项*/
            if (classFunc[j].getAttribute("id")=="closeFra")
            {
                classFunc[j].onclick=function(){ closeF('frame2');};
            }
            if (classFunc[j].getAttribute("id")=="closeMapGu")
            {
                classFunc[j].onclick=function(){

                    mapClose();
                    /*api.openWin({
                        name:'menu',
                        url:'../html/frame1.html',
                        hScrollBarEnabled:false,
                        vScrollBarEnabled:false,
                        scaleEnabled:true,
                        reload:true,
                        rect:{
                            x:0,
                            y:0,
                            w:api.winWidth,
                            h:api.winHeight
                        }
                    });*/

                            /*api.execScript({
                                name:'menu',
                                script:guChange()
                            });*/
                            closeF('mapGu');
                    };
            }
            if (classFunc[j].getAttribute("id")=="closeMapChen")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapChen');
                };
            }
            if (classFunc[j].getAttribute("id")=="closeMapLiao")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapLiao');
                };
            }
            if (classFunc[j].getAttribute("id")=="closeMapLu")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapLu');
                };
            }
            if (classFunc[j].getAttribute("id")=="closeMapQian")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapQian');
                };
            }
            if (classFunc[j].getAttribute("id")=="closeMapQin")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapQin');
                };
            }
            if (classFunc[j].getAttribute("id")=="closeMapShu")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapShu');
                };
            }
            if (classFunc[j].getAttribute("id")=="closeMapWen")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapWen');
                };
            }
            if (classFunc[j].getAttribute("id")=="closeMapXue")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapXue');
                };
            }
            if (classFunc[j].getAttribute("id")=="closeMapZhang")
            {
                classFunc[j].onclick=function(){
                    mapClose();
                    closeF('mapZhang');
                };
            }


            /*添加收藏选项，改变收藏图标的叠放次序*/
            if (classFunc[j].getAttribute("id")=="guCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("guCol","../image/collectEnd.png");
                    $api.setStorage('gu1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="chenCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("chenCol","../image/collectEnd.png");
                    $api.setStorage('chen1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="liaoCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("liaoCol","../image/collectEnd.png");
                    $api.setStorage('liao1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="luCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("luCol","../image/collectEnd.png");
                    $api.setStorage('lu1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="qianCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("qianCol","../image/collectEnd.png");
                    $api.setStorage('qian1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="qinCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("qinCol","../image/collectEnd.png");
                    $api.setStorage('qin1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="shuCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("shuCol","../image/collectEnd.png");
                    $api.setStorage('shu1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="wenCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("wenCol","../image/collectEnd.png");
                    $api.setStorage('wen1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="xueCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("xueCol","../image/collectEnd.png");
                    $api.setStorage('xue1','1');
                };
            }
            if (classFunc[j].getAttribute("id")=="zhangCol")
            {
                classFunc[j].onclick=function(){
                    srcChange("zhangCol","../image/collectEnd.png");
                    $api.setStorage('zhang1','1');
                };
            }


        }



        /*function guChange(){

            alert($("#guStr").attr("src"));
            $("#guStr").attr("src","../image/favPic.png");
            /!*alert($("#guStr").attr("src"));*!/
        }*/


        /*function lisPic(){
            if(api.addEventListener){
            api.addEventListener({
                name: 'myEvent'
            }, function(ret, err){
                if(ret.value){
                    alert(ret.value);
                }
            });
            }
        }*/




        /*监听收藏的index是否改变，若改变，则在关闭frame的同时修改收藏图标*/
        /*function listenIndex(theId,anotherId){
            var firId = document.getElementById(theId);
            var secId = document.getElementById(anotherId);
            if(firId.getAttribute("z-index")<secId.getAttribute("z-index"))
            {
                changeIndex(".guStr","z-index","5");
                changeIndex(".guStr","opacity","1");
            }
        }*/

        /*改变图片*/
        function srcChange(changeId,changeSrc){
            var srcWaitChange = document.getElementById(changeId);
            srcWaitChange.setAttribute("src",changeSrc);/*!!!!!!!!!!!!!!!!!!!!!!!!bug*/
        }

        /*关闭弹框*/
        function closeF(str){
            api.closeFrame({
                name: str
            });
        }

        /*改变css*/
      /*  function changeIndex(changeClass,changeAttribute,str){
            $(changeClass).css(changeAttribute,str);
            /!*$(otherClass).css("z-index","5");
            $(otherClass).css("opacity","1");*!/
            /!*alert("");*!/
        }*/




        function openF(){
            api.openFrame({
                    name:'frame2',
                    url:'../html/frame2.html',
                    rect:{
                        x:0, 
                        y:-250,
                        w:api.winWidth,
                        h:api.winHeight+250
                    },
                    animation:{
                        type:"flip",
                        subType:"from_bottom",
                        duration:1000
                    }
            });
        }


        /*进入时背景图片的锚点*/
        /*var cc = document.getElementById("ancFir");
        cc.scrollIntoView(true);*/



        function returnBgpic(){

            $("#bg2").fadeOut(1000);

            $("#music").css("opacity","1");
            $("#camera").css("opacity","1");
        }





        /*菜单按钮选项*/
        function menuStr(index){
            switch(index){
                case 0:{
                    lightAndAnimation("guStr",".guPic","10%");
                }
                    break;
                case 1:{
                    lightAndAnimation("chenStr",".chenPic","9%")
                }
                    break;
                case 2:{
                    lightAndAnimation("luStr",".luPic","9%")
                }
                    break;
                /*case 3:{
                    lightAndAnimation("qinqiStr",".qinqiPic","11%")
                }
                    break;*/
                case 3:{
                    lightAndAnimation("wenStr",".wenPic","8%")
                }
                    break;
                case 4:{
                    lightAndAnimation("shuStr",".shuPic","10%")
                }
                    break;
                case 5:{
                    lightAndAnimation("qinStr",".qinPic","7%")
                }
                    break;
                case 6:{
                    lightAndAnimation("xueStr",".xuePic","11%")
                }
                    break;
                /*case 8:{
                    lightAndAnimation("xuehuaStr",".xuehuaPic","8%")
                }
                    break;*/
                case 7:{
                    lightAndAnimation("qianStr",".qianPic","10%")
                }
                    break;
                case 8:{
                    lightAndAnimation("zhangStr",".zhangPic","8%")
                }
                    break;
                case 9:{
                    lightAndAnimation("liaoStr",".liaoPic","9%")
                }
                    break;
            }
        }
        /*点击菜单后，地标变大变小的动效*/
        function lightAndAnimation(id,cla,str){
            var guStr1 = document.getElementById(id);
            guStr1.scrollIntoView(true);
            $(cla).animate({
                height: '+=10px',
                width: '+=15px'
            },"slow");
            $(cla).animate({
                height: '-=10px',
                width: '-=15px'
            },"slow");
            $(cla).css("width",str);

        }

        function changeBgPic(){
            $("#bg2").fadeIn(1000);
            $("#music").css("opacity","0");
            $("#camera").css("opacity","0");
        }

            /*菜单*/
        function menuOp(){
                var arrayPath = [];
                arrayPath[0] = {
                    title : '顾毓琇故居',
                    icon : '../image/machine.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ffffff"
                };
                arrayPath[1] = {
                    title : '陈氏旧宅',
                    icon : 'widget://res/2.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#000000"
                };
                arrayPath[2] = {
                    title : '陆定一故居',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };
                /*arrayPath[3] = {
                    title : '秦起铜像',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };*/
                arrayPath[3] = {
                    title : '文渊坊',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };
                arrayPath[4] = {
                    title : '图书馆旧址',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };
                arrayPath[5] = {
                    title : '秦谷柳故居',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };
                arrayPath[6] = {
                    title : '薛汇东住宅',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };
                /*arrayPath[8] = {
                    title : '薛家花园',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };*/
                arrayPath[7] = {
                    title : '钱钟书故居',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };
                arrayPath[8] = {
                    title : '张闻天故居',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };
                arrayPath[9] = {
                    title : '繆公馆',
                    icon : 'widget://res/3.png',
                    bgColor : "rgba(220,220,220,0.8)",
                    highlightColor : "#ff0000"
                };
                var MNStack = api.require('MNStack');
                MNStack.open({
                    startCoords : {
                        x : api.winWidth-100,
                        y : 60
                    },
                    styles : {
                        bg : 'rgba(0,0,0,0.7)',
                        itemHeight : 50,
                        titleColor : '#000',
                        direction : 'left_down'
                    },
                    items : arrayPath
                }, function(ret, err) {
                    menuStr(ret.index);
                }); 
        }
    }
});




