---
layout: myzv
title: My Zenvera Search
heading: My Zenvera Search
subheading: Zenvera Player and Guild Search
icon: fa-trophy
---
{% raw %}
<div id="search"></div>
<fieldset>
<legend>Player Search</legend>
<form action="#" onsubmit="return PlayerSearch();">
<p><label for="term">Search Term: </label><input id="playerQ" type="text" name="playerQ" size="20"/></p><p><input type="submit" value="Search!"/></p>
<p>Enter a full or partial player name.  Searches must be at least 3 characters in length.</p>
</form>
</fieldset>
<fieldset>
<legend>Guild Search</legend>
<form action="#" onsubmit="return GuildSearch();">
<p><label for="term">Search Term: </label><input id="guildQ" type="text" name="guildQ" size="20"/></p><p><input type="submit" value="Search!"/></p>
<p>Enter a full or partial guild name, or guild abbreviation.</p>
</form>
</fieldset>
<script>
    function PlayerSearch() { 
        $.get('https://myzv.herokuapp.com/player-search.php?term=' + $("#playerQ"), function( data ) { $( '#search' ).html( data ); }); return false;
    }
    function GuildSearch() { 
        $.get('https://myzv.herokuapp.com/guild-search.php?term=' + $("#guildQ"), function( data ) { $( '#search' ).html( data ); }); return false;
    }
</script>
{% endraw %}