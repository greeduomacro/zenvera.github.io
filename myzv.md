---
layout: myzv
title: My Zenvera
heading: My Zenvera
subheading: MyZenvera is a portal to the world of Zenvera.
icon: fa-trophy
---
Use the menu options to search for any player or guild on the server, view the dueling rankings, check the current status of faction towns, and much more.
{% raw %}
<div id="myzv-stats">Loading...</div>
<script>$.get('https://myzv.herokuapp.com/status.php', function( data ) {$( '#myzv-stats' ).html( data ); });</script>
{% endraw %}