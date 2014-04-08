---
layout: myzv
title: My Zenvera
heading: My Zenvera
subheading: MyZenvera is a portal to the world of Zenvera. You can search for any player or guild on the server, view the dueling rankings, or check the current status of faction towns.
icon: fa-trophy
---
{% raw %}
<div id="myzv-stats">Loading</div>
<p id="guildsize"></p>
<p id="guildmurderers"></p>
<script>$.get('https://myzv.herokuapp.com/status.php', function( data ) {$( '#myzv-stats' ).append( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/guilds-size.php', function( data ) { $( '#guildsize' ).html( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/guilds-murderers.php', function( data ) { $( '#guildmurderers' ).html( data ); });</script>
{% endraw %}