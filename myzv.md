---
layout: myzv
title: My Zenvera
heading: My Zenvera
subheading: MyZenvera is a portal to the world of Zenvera.
icon: fa-trophy
---
Use the menu options to search for any player or guild on the server, view the dueling rankings, check the current status of faction towns, and more.
{% raw %}
<div id="myzv-stats">Loading...</div>
<script>
var myzv = ('https:' == document.location.protocol ? 'https://myzv.herokuapp.com/' : 'http://my.zenvera.com/');
$.get(myzv+'status.php', function(data) {$('#myzv-stats').html(data); });
</script>
{% endraw %}