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
<p><label for="term">Search Term: </label><input id="playerQ" type="text" name="playerQuery" size="20"/></p><p><input name="submit" onclick='PlayerSearch();' value="Search!"/></p>
<p>Enter a full or partial player name.  Searches must be at least 3 characters in length.</p>
</form>
</fieldset>
<fieldset>
<legend>Guild Search</legend>
<form action="#" onsubmit="return GuildSearch();">
<p><label for="term">Search Term: </label><input id="guildQ" type="text" name="guildQuery" size="20"/></p><p><input name="submit" onclick='GuildSearch();' value="Search!"/></p>
<p>Enter a full or partial guild name, or guild abbreviation.</p>
</form>
</fieldset>
<script>
    function PlayerSearch() { 
        $.get('https://myzv.herokuapp.com/player-search.php?term=' + $("#playerQuery").val(), function( data ) { $( '#search' ).html( data ); }); return false;
    }
    function GuildSearch() { 
        $.get('https://myzv.herokuapp.com/guild-search.php?term=' + $("#guildQuery").val(), function( data ) { $( '#search' ).html( data ); }); return false;
    }
</script>
{% endraw %}