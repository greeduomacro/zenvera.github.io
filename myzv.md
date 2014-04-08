---
layout: myzv
title: My Zenvera
heading: My Zenvera
subheading: MyZenvera is a portal to the world of Zenvera. You can search for any player or guild on the server, view the dueling rankings, or check the current status of faction towns.
icon: fa-trophy
---
{% raw %}
<p id="guildsize"></p>
<p id="playerduel"></p>
<p id="playermurderers"></p>
<p id="guildmurderers"></p>
<script>$.get('https://myzv.herokuapp.com', function( data ) { $( '#psubheading' ).append( " " ); $( '#psubheading' ).append( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/guilds-size.php', function( data ) { $( '#guildsize' ).html( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/players-duelists.php', function( data ) { $( '#playerduel' ).html( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/players-murderers.php', function( data ) { $( '#playermurderers' ).html( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/guilds-murderers.php', function( data ) { $( '#guildmurderers' ).html( data ); });</script>
{% endraw %}