---
layout: article
heading: Account Management
subheading: The following forms can be used to reset your account password or retrieve a list of account names.
icon: fa-lock
---
{% raw %}
<div id="recovery"></div>
<script>$.get("https://zenvera.herokuapp.com/recovery.php", function( data ) { $( "#recovery" ).html( data ); });</script>
<br/>
{% endraw %}