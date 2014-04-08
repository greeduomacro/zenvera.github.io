---
layout: myzv
title: My Zenvera Factions
heading: My Zenvera Factions
subheading: Zenvera Faction Status
icon: fa-trophy
---
{% raw %}
<p id="factions"></p>
<script>$.get('https://myzv.herokuapp.com/factions.php', function( data ) { $( '#factions' ).html( data ); });</script>
{% endraw %}