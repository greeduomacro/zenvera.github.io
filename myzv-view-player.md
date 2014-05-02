---
layout: myzv
title: My Zenvera Player Details
heading: My Zenvera Player Details
subheading:
icon: fa-trophy
---
{% raw %}
<!--<div id="paperdoll" style="float: right;">Loading...</div>-->
<div id="details">Loading...</div>
<script src="//cdnjs.cloudflare.com/ajax/libs/jquery-url-parser/2.3.1/purl.min.js"></script>
<script>
    $(document).ready( function() {
        var myzv = ('https:' == document.location.protocol ? 'https://myzv.herokuapp.com/' : 'http://my.zenvera.com/');
        var id = $.url().param('id');
        $('#mheader').css('padding-top', '0');
        $('#page-icon').html('<img src="'+myzv+'myzv-img/character.php?id='+id+'" alt="Player Image"/>' );
        <!--$.get(myzv+'view-paperdoll.php?id='+id, function(data) { $('#paperdoll').html(data); });-->
        $.get(myzv+'view-player.php?id='+id, function(data) { $('#details').html(data); $('#pheading').text( $('#name-value').text() ); $('#psubheading').html( $('#guild-value').html() ); });
    });
</script>
{% endraw %}