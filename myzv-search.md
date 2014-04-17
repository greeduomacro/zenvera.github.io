---
layout: myzv
title: My Zenvera Search
heading: My Zenvera Search
subheading: Zenvera Player and Guild Search
icon: fa-trophy
---
{% raw %}
<fieldset style="float: left;">
<form action="#" onsubmit="return PlayerSearch();">
<p><label for="playerQ">Player Search:</label><input id="playerQ" type="text" name="playerQuery" size="20" style="width: auto; padding: 0;"/><input type="submit" onclick='PlayerSearch();' value="Search!"/></p>
</form>
</fieldset>
<fieldset>
<form action="#" onsubmit="return GuildSearch();">
<p><label for="guildQ">Guild Search:</label><input id="guildQ" type="text" name="guildQuery" size="20" style="width: auto; padding: 0;"/><input type="submit" onclick='GuildSearch();' value="Search!"/></p>
</form>
</fieldset>
<div id="results">Enter a full or partial player name. Searches must be at least 3 characters in length. Enter a full or partial guild name, or guild abbreviation.</div>
<script src="js/purl.js"></script>
<script>
    $(document).ready( function() {
        var t = $.url().param('t');
        var q = $.url().param('q');
        if (t == 'p') {
            $("#playerQ").val(q);
            PlayerSearch();
        } else if (t == 'g') {
            $("#guildQ").val(q);
            GuildSearch();
        }
    });
    function PlayerSearch() { 
        $.get('//myzv.herokuapp.com/player-search.php?term=' + $("#playerQ").val(), function( data ) { $( '#results' ).html( data ); }); return false;
    }
    function GuildSearch() { 
        $.get('//myzv.herokuapp.com/guild-search.php?term=' + $("#guildQ").val(), function( data ) { $( '#results' ).html( data ); }); return false;
    }
</script>
{% endraw %}