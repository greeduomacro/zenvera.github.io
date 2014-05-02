---
layout: myzv
title: My Zenvera Guild Details
heading: My Zenvera Guild Details
subheading:
icon: fa-trophy
---
{% raw %}
<div id="details">Loading...</div>
<script src="//cdnjs.cloudflare.com/ajax/libs/jquery-url-parser/2.3.1/purl.min.js"></script>
<script>
    $(document).ready( function() {
        var id = $.url().param('id');
        $.get('//myzv.herokuapp.com/view-guild.php?id=' + id, function( data ) { $( '#details' ).html( data ); });
    });
</script>
{% endraw %}