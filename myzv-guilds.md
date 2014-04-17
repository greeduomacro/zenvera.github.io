---
layout: myzv
title: My Zenvera Guilds
heading: My Zenvera Guilds
subheading: Zenvera Guild Status
icon: fa-trophy
---
{% raw %}
<div style="float: left;">
<fieldset>
<legend><strong>Largest Guilds</strong></legend>
<div id="largest-guilds">Loading...</div>
</fieldset>
</div>
<div style="float: left;">
<fieldset>
<legend><strong>Top Murdering Guilds</strong></legend>
<div id="murdering-guilds">Loading...</div>
</fieldset>
</div>
<div style="float: left;">
<fieldset>
<legend><strong>Top Warring Guilds</strong></legend>
<div id="warring-guilds">Loading...</div>
</fieldset>
</div>
<p style="clear: both;"></p>
<script>$.get('//myzv.herokuapp.com/guild-size-rankings.php', function( data ) { $( '#largest-guilds' ).html( data ); });</script>
<script>$.get('//myzv.herokuapp.com/guild-murder-rankings.php', function( data ) { $( '#murdering-guilds' ).html( data ); });</script>
<script>$.get('//myzv.herokuapp.com/guild-wars-rankings.php', function( data ) { $( '#warring-guilds' ).html( data ); });</script>
{% endraw %}