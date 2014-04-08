---
layout: myzv
title: My Zenvera Poker Hand Details
heading: My Zenvera Poker Hand Details
subheading:
icon: fa-trophy
---
{% raw %}
<div id="details">Loading...</div>
<script src="js/purl.js"></script>
<script>
    $(document).ready( function() {
        var id = $.url().param('id');
        $.get('https://myzv.herokuapp.com/poker-hand.php?id=' + id, function( data ) { $( '#details' ).html( data ); });
    });
</script>
{% endraw %}