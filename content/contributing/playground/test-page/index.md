---
title: "Test Page"
description: ""
lead: ""
date: 2021-05-22T19:48:56+01:00
lastmod: 2021-05-22T19:48:56+01:00
draft: false
images: []
menu: 
  contributing:
    parent: "playground"
weight: 998
toc: true
---

<!-- Tribe Tag -->
<script>
  (function(t,r,i,b,e){
    if(typeof t.Tribe==='function'){t.Tribe('reload',{portal:i});}
    else{b=function(){b.r(arguments);};b.q=[];b.r=function(args){b.q.push(args);};
    t.Tribe=b; e=r.createElement('script');e.type='text/javascript';e.async=true;
    e.src=i+'/widget/v1/main.js?t='+Math.ceil(new Date() / 3e5) * 3e5;
    var x=r.getElementsByTagName('script')[0];x.parentNode.insertBefore(e,x);
    t.Tribe('boot',{portal:i});}
  })(window,document,'{https://jitsuin.tribe.so}');
</script>

<div id="topic-widget"></div>
<script>
  window.Tribe('topic', {
    id: 'topic-widget',     
    slug: 'test-topic',
    components: ['breadcrumb', 'sidebar', 'header', 'suggestions', 'input'],
    feedLimit: 5
  })
</script>