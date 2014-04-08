---
layout: myzv
title: My Zenvera Search
heading: My Zenvera Search
subheading: Zenvera Player and Guild Search
icon: fa-trophy
---
{% raw %}
<fieldset>
<legend>Player Search</legend>
<form action="/myzv-player-search/" method="get">
<p><label for="term">Search Term: </label><input id="term" type="text" name="term" size="20"/></p><p><input type="submit" value="Search!"/></p>
<p>Enter a full or partial player name.  Searches must be at least 3 characters in length.</p>
</form>
</fieldset>
<fieldset>
<legend>Guild Search</legend>
<form action="/myzv-guild-search/" method="get">
<p><label for="term">Search Term: </label><input id="term" type="text" name="term" size="20"/></p><p><input type="submit" value="Search!"/></p>
<p>Enter a full or partial guild name, or guild abbreviation.</p>
</form>
</fieldset>
<p id="poker"></p>
<script>$.get('https://myzv.herokuapp.com/poker.php', function( data ) { $( '#poker' ).html( data ); });</script>
{% endraw %}