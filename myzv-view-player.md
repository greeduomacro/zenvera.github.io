---
layout: myzv
title: My Zenvera Player Details
heading: My Zenvera Player Details
subheading:
icon: fa-trophy
---
{% raw %}
<div id="details">Loading...</div>
<script src="js/purl.js"></script>
<script>
    $(document).ready( function() {
        var id = $.url().param('id');
        $.get('https://myzv.herokuapp.com/view-player.php?id=' + id, function( data ) { $( '#details' ).html( data ); $('#pheading').html($('#name-value').val());});
    });
</script>
{% endraw %}