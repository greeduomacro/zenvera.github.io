---
layout: myzv
title: My Zenvera Poker
heading: My Zenvera Poker
subheading: Zenvera Poker Statistics
icon: fa-trophy
---
Zenvera tracks every poker game played within the world.
{% raw %}
<div id="poker-status">Loading...</div>
<div style="float: left;">
<fieldset>
<legend><strong>Latest Low-Rollers</strong></legend>
<div id="poker-lowrollers">Loading...</div>
</fieldset>
</div>
<div style="position: relative; margin-left: 300px;">
<fieldset>
<legend><strong>Latest High-Rollers</strong></legend>
<div id="poker-highrollers">Loading...</div>
</fieldset>
</div>
<div style="clear: both;"></div>
<div style="float: left;">
<fieldset>
<legend><strong>Largest Laydowns</strong></legend>
<div id="poker-laydowns">Loading...</div>
</fieldset>
</div>
<div style="position: relative; margin-left: 300px;">
<fieldset>
<legend><strong>Largest Showdowns</strong></legend>
<div id="poker-showdowns">Loading...</div>
</fieldset>
</div>
<div style="clear: both;"></div>
<div style="float: left;">
<fieldset>
<legend><strong>Poker Sharks</strong></legend>
<div id="poker-sharks">Loading...</div>
</fieldset>
</div>
<div style="position: relative; margin-left: 300px;">
<fieldset>
<legend><strong>Poker Fishes</strong></legend>
<div id="poker-fishes">Loading...</div>
</fieldset>
</div>
<script>
var myzv = ('https:' == document.location.protocol ? 'https://myzv.herokuapp.com/' : 'http://my.zenvera.com/');
$.get(myzv+'poker-status.php', function(data) { $('#poker-status').html(data); });
$.get(myzv+'poker-latest-low-rollers.php', function(data) { $('#poker-lowrollers').html(data); });
$.get(myzv+'poker-latest-high-rollers.php', function(data) { $('#poker-highrollers').html(data); });
$.get(myzv+'poker-largest-laydowns.php', function(data) { $('#poker-laydowns').html(data); });
$.get(myzv+'poker-largest-showdowns.php', function(data) { $('#poker-showdowns').html(data); });
$.get(myzv+'poker-sharks.php', function( data ) { $('#poker-sharks').html(data); });
$.get(myzv+'poker-fishes.php', function( data ) { $('#poker-fishes').html(data); });
</script>
{% endraw %}