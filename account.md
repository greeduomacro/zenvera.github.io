---
layout: article
title: Zenvera Account Management
heading: Account Management
subheading: The following forms can be used to reset your account password or retrieve a list of account names.
icon: fa-lock
---
{% raw %}
<div>
    <fieldset>
    <legend>Password Reset</legend>
    <form action="https://zenvera.herokuapp.com/recovery.php" method="POST">
        <table style="width: 40%;">
            <tr><td align="left"><input id="account" type="text" name="account" placeholder="Account Name" size="20" maxlength="32"/></td></tr>
            <tr><td align="left"><input id="email" type="text" name="email" placeholder="E-Mail Address" length="20" maxlength="320"/></td></tr>
            <tr><td align="center"><input id="reqtype" type="hidden" name="reqtype" value="passwordreset"><input type="submit" value="Submit"/></td></tr>
        </table>
    </form>
    </fieldset>
</div>
{% endraw %}        
        
### Please Note

* After submitting this form you will receive an e-mail with instructions on how to validate your request.
* Only accounts with a registered e-mail address can be reset.
* Accounts that have decayed due to inactivity are unrecoverable and cannot be reset.
* Banned accounts cannot be reset.
* You are limited to three reset requests every two hours, even if they are unsuccessful.
* Your request will be silently ignored if invalid information is submitted, if you have any pending account requests, or if you exceed the number of allowed attempts.
* Requests must be validated within 2 hours of receipt and automatically expire at server wars. 
* If your validation expires, submit a new request.
* Any requests received when the server is down or during server wars are processed upon restart.
* This system is heavily monitored. The IP address of every request and validation (successful or not) is logged.
* Abuse of this system will result in being firewalled across the network.


{% raw %}
<div>
    <fieldset>
    <legend>Forgot Account</legend>
    <form action="https://zenvera.herokuapp.com/recovery.php" method="POST">
        <table style="width: 40%;">
            <tr><td align="left"><input id="email" type="text" name="email" placeholder="E-Mail Address" length="20" maxlength="320"/></td></tr>
            <tr><td align="center"><input id="reqtype" type="hidden" name="reqtype" value="accountnames"><input type="submit" value="Submit"/></td></tr>
        </table>
    </form>
    </fieldset>
</div>
{% endraw %}

### Please Note:

* After submitting this form you will receive an e-mail containing a list of account names registered with your e-mail address.
* You are limited to one request per e-mail address and five requests in total every two hours.
* Your request will be silently ignored if invalid information is submitted or if you exceed the number of allowed attempts.
* Any requests received when the server is down or during server wars are processed upon restart.
* This system is heavily monitored. The IP address of every request is logged.
* Abuse of this system will result in being firewalled across the network.
