---
layout: myzv
heading: My Zenvera Guilds
subheading: Zenvera Guild Status
icon: fa-trophy
---
{% raw %}
<p id="guilds"></p>
<script>$.get('https://my-zvx.rhcloud.com/guilds.php', function( data ) { $( '#guilds' ).html( data ); });</script>
{% endraw %}