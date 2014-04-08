---
layout: myzv
title: My Zenvera Factions
heading: My Zenvera Factions
subheading: Zenvera Faction Status
icon: fa-trophy
---
{% raw %}
<div style="float: left;">
<fieldset>
<legend><strong>Faction Rankings</strong></legend>
<div id="faction-rankings">Loading...</div>
</fieldset>
</div>
<div style="float:right;">
<fieldset>
<legend><strong>Player Rankings</strong></legend>
<div id="faction-player-rankings">Loading...</div>
</fieldset>
</div>
<div style="float:left; margin-top: 50px;">
<fieldset>
<legend><strong>Guild Rankings</strong></legend>
<div id="faction-guild-rankings">Loading...</div>
</fieldset>
</div>
<div style="clear: both; position: relative; top: 50px;">
<fieldset>
<legend><strong>Town Status</strong></legend>
<div id="town-status">Loading...</div>
</fieldset>
</div>
<p style="clear: both; text-align: right; margin-top: 50px; font-size: 80%;">Icons &copy; Electronics Arts, Inc.</p>
<script>$.get('https://myzv.herokuapp.com/faction-rankings.php', function( data ) { $( '#faction-rankings' ).html( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/faction-player-rankings.php', function( data ) { $( '#faction-player-rankings' ).html( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/faction-guild-rankings.php', function( data ) { $( '#faction-guild-rankings' ).html( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/faction-town-status.php', function( data ) { $( '#town-status' ).html( data ); });</script>
{% endraw %}