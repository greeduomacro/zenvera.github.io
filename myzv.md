---
layout: myzv
heading: My Zenvera
subheading: MyZenvera is a portal to the world of Zenvera. You can search for any player or guild on the server, view the dueling rankings, or check the current status of faction towns.
icon: fa-trophy
---
{% raw %}
<script>$.get('https://my-zvx.rhcloud.com', function( data ) { $( '#psubheading' ).append( " " ); $( '#psubheading' ).append( data ); });</script>
<script>$.get('https://my-zvx.rhcloud.com/players-murderers.php', function( data ) { $( '#murderers' ).html( data ); });</script>
{% endraw %}