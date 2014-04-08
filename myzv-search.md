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
<form action="#" onsubmit="return PlayerSearch();">
<p><label for="playerQ">Search Term: </label><input id="playerQ" type="text" name="playerQuery" size="20"/><input type="submit" onclick='PlayerSearch();' value="Search!"/></p>
</form>
</fieldset>
<fieldset>
<legend>Guild Search</legend>
<form action="#" onsubmit="return GuildSearch();">
<p><label for="guildQ">Search Term: </label><input id="guildQ" type="text" name="guildQuery" size="20"/><input type="submit" onclick='GuildSearch();' value="Search!"/></p>
</form>
</fieldset>
<p>Enter a full or partial player name. Searches must be at least 3 characters in length. Enter a full or partial guild name, or guild abbreviation.</p>
<div id="results"></div>
<script>
    function PlayerSearch() { 
        $.get('https://myzv.herokuapp.com/player-search.php?term=' + $("#playerQ").val(), function( data ) { $( '#results' ).html( data ); }); return false;
    }
    function GuildSearch() { 
        $.get('https://myzv.herokuapp.com/guild-search.php?term=' + $("#guildQ").val(), function( data ) { $( '#results' ).html( data ); }); return false;
    }
</script>
{% endraw %}