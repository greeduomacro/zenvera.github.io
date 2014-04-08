---
layout: myzv
heading: My Zenvera Factions
subheading: Zenvera Faction Status
icon: fa-trophy
---
{% raw %}
<p id="factions"></p>
<script>$.get('https://my-zvx.rhcloud.com/factions.php', function( data ) { $( '#factions' ).html( data ); });</script>
{% endraw %}