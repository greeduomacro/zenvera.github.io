---
layout: myzv
title: My Zenvera Player Details
heading: My Zenvera Player Details
subheading:
icon: fa-trophy
---
{% raw %}
<div id="paperdoll" style="float: right;">Loading...</div>
<div id="details">Loading...</div>
<script src="js/purl.js"></script>
<script>
    $(document).ready( function() {
        var id = $.url().param('id');
        $('#mheader').css('padding-top', '0');
        $('#page-icon').html('<img src="https://myzv.herokuapp.com/myzv-img/character.php?id=' + id + '" alt="Player Image"/>' );
        $.get('https://myzv.herokuapp.com/view-paperdoll.php?id=' + id, function( data ) { $( '#paperdoll' ).html( data ); });
        $.get('https://myzv.herokuapp.com/view-player.php?id=' + id, function( data ) { $( '#details' ).html( data ); $('#pheading').text( $('#name-value').text() ); $('#psubheading').html( $('#guild-value').html() ); });
    });
</script>
{% endraw %}