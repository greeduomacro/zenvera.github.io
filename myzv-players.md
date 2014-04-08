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
<legend><strong>Top Duelists</strong></legend>
<div id="player-dueling">Loading...</div>
</fieldset>
</div>
<div style="float: right;">
<fieldset>
<legend><strong>Top Murderers</strong></legend>
<div id="player-murderers">Loading...</div>
</fieldset>
</div>
<p style="clear: both;"></p>
<script>$.get('https://myzv.herokuapp.com/player-dueling-rankings.php', function( data ) { $( '#player-dueling' ).html( data ); });</script>
<script>$.get('https://myzv.herokuapp.com/player-murder-rankings.php', function( data ) { $( '#player-murderers' ).html( data ); });</script>
{% endraw %}