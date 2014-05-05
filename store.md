---
layout: article
title: Zenvera Store
heading: Store
subheading: Zenvera is completely free to play. We rely on purchases from the Zenvera store to offset project expenses.
icon: fa-usd
---

{% raw %}

<noscript>Please enable JavaScript before attempting to place an order.</noscript>

<script type='text/javascript'>
    $(document).ready( function() {
        $('#pp-btn').attr('disabled', false);
        $('#a-btn').attr('disabled', false);
    });

    function EnsureAccount(fId) {
        var a = $('#account-name').val().trim();
        if(!a.length) {
            return false;
        }
        
        $(fId).val(a);
        return true;
   }
</script>

<div>
    <fieldset>
        <legend><strong>Account Name</strong></legend>
        <div style="width: 280px; border: 2px; border-style: solid; border-color: red;">
                <input type="text" name="account-name" id="account-name" maxlength="32" placeholder="Account Name">
        </div>
    </fieldset>
</div>

<p></p>

<div style="width: 250px; height: 120px; float: left;">
    <fieldset>
    <legend><strong>PayPal</strong></legend>
    <form action="https://www.paypal.com/cgi-bin/webscr" onsubmit='return EnsureAccount("#p-a");' method="post" target="_top">
        <input type="hidden" name="cmd" value="_s-xclick">
        <input type="hidden" name="hosted_button_id" value="J4QQMTXMQYS7N">
        <div>
            <input type="hidden" name="on0" value="Zenvera Points">
            <div style="display: inline-block;">
                <select name="os0">
                    <option value="500 ZP">500 ZP $5.00 USD</option>
                    <option value="1100 ZP">1100 ZP $10.00 USD</option>
                    <option value="2400 ZP">2400 ZP $20.00 USD</option>
                    <option value="6500 ZP">6500 ZP $50.00 USD</option>
                </select>
                <input type="hidden" name="on1" value="Account Name">
                <input type="hidden" name="os1" id="p-a">
                <div style="text-align: center;">
                    <input type="hidden" name="currency_code" value="USD">
                    <input id="pp-btn" disabled="true" type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_buynowCC_LG.gif" border="0" name="submit" alt="PayPal - The safer, easier way to pay online!">
                    <img alt="" border="0" src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif" width="1" height="1">
                </div>
            </div>
        </div>
    </form>
    </fieldset>
</div>

<div style="width: 250px; height: 120px; float: left;">
    <fieldset>
    <legend><strong>Amazon Payments</strong></legend>
    <form action="https://zenvera.herokuapp.com/store/store-amazon.php" onsubmit='return EnsureAccount("#a-a");' method="post" target="_top">
        <div>
            <input type="hidden" name="on0" value="Zenvera Points">
            <div style="display: inline-block;">
                <select name="os0">
                    <option value="100 ZP">100 ZP $1.00 USD</option>
                    <option selected="selected" value="500 ZP">500 ZP $5.00 USD</option>
                    <option value="1100 ZP">1100 ZP $9.99 USD</option>
                    <option value="2400 ZP">2400 ZP $20.00 USD</option>
                    <option value="6500 ZP">6500 ZP $50.00 USD</option>
                    <option value="14000 ZP">14000 ZP $100.00 USD</option>
                </select>
                <input type="hidden" name="on1" value="Account Name">
                <input type="hidden" name="os1" id="a-a">
                <div style="text-align: center;"><input id="a-btn" disabled="true" type="image" src="https://authorize.payments.amazon.com/pba/images/payNowButton.png" border="0" name="submit" alt="Amazon Payments"></div>
            </div>
        </div>
    </form>
    </fieldset>
</div>

<script src="https://checkout.google.com/inapp/lib/buy.js"></script>
<script type='text/javascript'>
    function RunButton() {
        if (!EnsureAccount('#g-a'))
            return false;

        $.post( "https://zenvera.herokuapp.com/store/google/generateJWT.php", $("#googleWalletForm").serialize(), function( data ) {
        google.payments.inapp.buy({ jwt: data.genJWT, success: function() {console.log('success');}, failure: function(result) {console.log(result.response.errorType);} }); }, "json"); return false; 
    }
</script>
<div style="width: 250px; height: 120px; float: left;">
    <fieldset>
    <legend><strong>Google Wallet</strong></legend>
    <form action="#" onsubmit="return RunButton();" id="googleWalletForm">
        <div>
            <div style="display: inline-block;">
                <select name="os0">
                    <option value="100 ZP">100 ZP $1.00 USD</option>
                    <option selected="selected" value="500 ZP">500 ZP $5.00 USD</option>
                    <option value="1100 ZP">1100 ZP $9.99 USD</option>
                    <option value="2400 ZP">2400 ZP $20.00 USD</option>
                    <option value="6500 ZP">6500 ZP $50.00 USD</option>
                </select>
                <input type="hidden" name="os1" id="g-a">
                <div style="text-align: center;"><img src="//storage.googleapis.com/cdn-1.appspot.com/zv/images/buy-button.png" width="152" border="0" alt="Google Wallet" id='buyButton' value='buy' onclick='RunButton();'></div>
            </div>
        </div>
    </form>
    </fieldset>
</div>

<script src="https://coinbase.com/assets/button.js" type="text/javascript"></script>
<!--
    100 => 1.00 => 94f92b90f6eeead5e2f8c2f92e3be71d
    500 => 5.00 => ff23c9b7df316e8d4804c1987be2b378
    1100 => 9.99 => bd472c1711b2203a3d5efda3772ca29a
    2400 => 20.00 => 5f9e4be8fcf20dd3ba12aba8cddba8e9
    6500 => 50.00 => f6354bfb4082a2335a192956b8a67775
-->
<script type='text/javascript'>
    function RunCoinbaseButton() {
        if (!EnsureAccount('#c-a'))
            return false;

        var cn = $('#c-a').val().trim();
        var camt = $('#c-amt').val().trim();
        
        var data = '';
        switch(camt) {
            case '100': data = '94f92b90f6eeead5e2f8c2f92e3be71d'; break;
            case '500': data = 'ff23c9b7df316e8d4804c1987be2b378'; break;
            case '1100': data = 'bd472c1711b2203a3d5efda3772ca29a'; break;
            case '2400': data = '5f9e4be8fcf20dd3ba12aba8cddba8e9'; break;
            case '6500': data = 'f6354bfb4082a2335a192956b8a67775'; break;
            default: return false;
        }
        
        $('.coinbase-button').attr('data-custom', cn);
        $(document).trigger('coinbase_show_modal', data);
        return false;
    }
</script>
<div style="width: 250px; height: 120px; float: left;">
    <fieldset>
    <legend><strong>Bitcoin</strong></legend>
    <form action="#" onsubmit="return RunCoinbaseButton();">
        <div>
            <div style="display: inline-block;">
                <select name="os0" id="c-amt">
                    <option value="100">100 ZP $1.00 USD</option>
                    <option selected="selected" value="500">500 ZP $5.00 USD</option>
                    <option value="1100">1100 ZP $9.99 USD</option>
                    <option value="2400">2400 ZP $20.00 USD</option>
                    <option value="6500">6500 ZP $50.00 USD</option>
                </select>
                <input type="hidden" name="os1" id="c-a">
                <div style="text-align: center;"><img src="https://coinbase.com/assets/buttons/buy_now_small.png" border="0" id="c-btn" alt="Bitcoin" value='buy' onclick='RunCoinbaseButton();'></div>
                <div class="coinbase-button" data-code="94f92b90f6eeead5e2f8c2f92e3be71d" data-button-style="none"></div>
                <div class="coinbase-button" data-code="ff23c9b7df316e8d4804c1987be2b378" data-button-style="none"></div>
                <div class="coinbase-button" data-code="bd472c1711b2203a3d5efda3772ca29a" data-button-style="none"></div>
                <div class="coinbase-button" data-code="5f9e4be8fcf20dd3ba12aba8cddba8e9" data-button-style="none"></div>
                <div class="coinbase-button" data-code="f6354bfb4082a2335a192956b8a67775" data-button-style="none"></div>
            </div>
        </div>
    </form>
    </fieldset>
</div>
<br style="clear: both;">

{% endraw %}

__Please double check your account name before placing your order.__
Your items will be available to characters on the account name you provide during checkout as soon as the transaction clears.
You can access the Zenvera redemption system in-game by typing [zenvera at any time or by double-clicking one of the Zenvera stones throughout the world.

Purchased items have no real world value. Due to the nature of the game Zenvera cannot be responsible for nor replace lost or stolen items.

If you require assistance with your order please feel free to e-mail support@zenvera.com.

{% raw %}
<script type='text/javascript'>
    $(document).ready( function() {
        var zv = ('https:' == document.location.protocol ? 'https://zenvera.herokuapp.com/' : 'http://api.zenvera.com/');
        $.get(zv+'store/current.php', function(data) {
            $('#item-list').html(data);
        });
    });
</script>
{% endraw %}

#### Random Items

<div id="item-list"></div>
<div style="clear: both;"></div>