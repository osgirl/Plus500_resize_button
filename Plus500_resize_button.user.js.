// ==UserScript==
// @name         Plus 500 resize button
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Plus 500 resize button
// @author       chg.hou
// @match        https://app.plus500.com/trade/*
// @grant        none
// @run-at       document-idle
// ==/UserScript==

function waitForFnc_a() {

    if (document.getElementsByClassName('zoom').length===0 || document.getElementById('trading-group')==null || document.getElementById('graph-group')==null)
    {
        window.setTimeout(waitForFnc_a,1000);
        return;
    }
    var zoom_group = document.getElementsByClassName('zoom')[0];
    var  a1=document.createElement('button');
    var  a2=document.createElement('button');
    //a.className = 'icon-minimize';
    //a.className = 'close';
    a1.className = 'icon-search-minus';
    a2.className = 'icon-search-plus';

    a1.title="enlarge";
    a2.title="restore";

    zoom_group.appendChild(a1);
    zoom_group.appendChild(a2);

    a1.onclick = function(){

        var b = document.getElementById('trading-group');
        b.style.height = '20%';
        b.style.minHeight = '20%';
        b.style.maxHeight = '20%';

        var c = document.getElementById('graph-group');
        c.style.height = '80%';
        c.style.minHeight = '80%';
        c.style.maxHeight = '80%';

        var d = document.getElementById('highcharts-0');
        d.style.height = '600px';

        window.dispatchEvent(new Event('resize'));
    };
    a2.onclick = function(){


        var b = document.getElementById('trading-group');
        b.style.height = '40%';
        b.style.minHeight = '40%';
        b.style.maxHeight = '40%';

        var c = document.getElementById('graph-group');
        c.style.height = '60%';
        c.style.minHeight = '60%';
        c.style.maxHeight = '60%';

        var d = document.getElementById('highcharts-0');
        d.style.height = '300px';

        window.dispatchEvent(new Event('resize'));
    };


}

window.setTimeout(waitForFnc_a,3000);
