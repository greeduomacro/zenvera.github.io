---
layout: article
title: Zenvera Store
heading: Store
subheading: Zenvera is completely free to play. We rely on purchases from the Zenvera store to offset project expenses.
icon: fa-usd
---
{% raw %}
<div style="margin-left=auto;margin-right=auto;float:left;">
    <fieldset>
    <legend><b>PayPal</b></legend>
    <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
        <input type="hidden" name="cmd" value="_s-xclick">
        <input type="hidden" name="hosted_button_id" value="J4QQMTXMQYS7N">
        <table>
            <tr><td><input type="hidden" name="on0" value="Zenvera Points">Zenvera Points</td></tr><tr><td><select name="os0">
                <option value="500 ZP">500 ZP $5.00 USD</option>
                <option value="1100 ZP">1100 ZP $10.00 USD</option>
                <option value="2400 ZP">2400 ZP $20.00 USD</option>
                <option value="6500 ZP">6500 ZP $50.00 USD</option>
            </select> </td></tr>
            <tr><td><input type="hidden" name="on1" value="Account Name">Account Name</td></tr><tr><td><input type="text" name="os1" maxlength="200"></td></tr>
        </table>
        <div align="center">
            <input type="hidden" name="currency_code" value="USD">
            <input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_buynowCC_LG.gif" border="0" name="submit" alt="PayPal - The safer, easier way to pay online!">
            <img alt="" border="0" src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif" width="1" height="1">
        </div>
    </form>
    </fieldset>
</div>
<div style="margin-left=auto;margin-right=auto;float:left;">
    <fieldset>
    <legend><b>Amazon Payments</b></legend>
    <form action="https://zvwapi.appspot.com/store-amazon.php" method="post" target="_top">
        <table>
        <tr><td><input type="hidden" name="on0" value="Zenvera Points">Zenvera Points</td></tr><tr><td><select name="os0">
            <option value="100 ZP">100 ZP $1.00 USD</option>
            <option value="500 ZP">500 ZP $5.00 USD</option>
            <option value="1100 ZP">1100 ZP $9.99 USD</option>
            <option value="2400 ZP">2400 ZP $20.00 USD</option>
            <option value="6500 ZP">6500 ZP $50.00 USD</option>
        </select> </td></tr>
        <tr><td><input type="hidden" name="on1" value="Account Name">Account Name</td></tr><tr><td><input type="text" name="os1" maxlength="200"></td></tr>
        </table>
        <div align="center">
            <input type="image" src="https://authorize.payments.amazon.com/pba/images/payNowButton.png" border="0" name="submit" alt="Amazon Payments">
        </div>
    </form>
    </fieldset>
</div>
<script src="https://checkout.google.com/inapp/lib/buy.js"></script>
<script type='text/javascript'>
    function RunButton() { $.post( "https://zvwapi.appspot.com/google/generateJWT.php", $("#googleWalletForm").serialize(), function( data ) {
        google.payments.inapp.buy({ jwt: data.genJWT, success: function() {console.log('success');}, failure: function(result) {console.log(result.response.errorType);} }); }, "json"); return false; 
    }
</script>
<div style="margin-left=auto;margin-right=auto;float:left;">
    <fieldset>
        <legend><b>Google Wallet</b></legend>
        <form action="#" onsubmit="return RunButton();" id="googleWalletForm">
        <table>
        <tr><td><input type="hidden" name="on0" value="Zenvera Points">Zenvera Points</td></tr><tr><td><select name="os0">
                <option value="100 ZP">100 ZP $1.00 USD</option>
                <option value="500 ZP">500 ZP $5.00 USD</option>
                <option value="1100 ZP">1100 ZP $9.99 USD</option>
                <option value="2400 ZP">2400 ZP $20.00 USD</option>
                <option value="6500 ZP">6500 ZP $50.00 USD</option>
        </select> </td></tr>
        <tr><td><input type="hidden" name="on1" value="Account Name">Account Name</td></tr><tr><td><input type="text" name="os1" maxlength="200"></td></tr>
        </table>
        <div align="center">
        <!--<img src="https://checkout.google.com/buttons/checkoutMobile.gif?merchant_id=176727849928054&w=152&h=30&style=white&variant=no-text&loc=en_US" border="0" alt="Google Wallet" id='buyButton' value='buy' onclick='RunButton();'>-->
            <img src="https://zenvera.com/images/buy-button.png" width="152" border="0" alt="Google Wallet" id='buyButton' value='buy' onclick='RunButton();'>
        </div>
    </form>
    </fieldset>
</div>
<div style="margin-left=auto;margin-right=auto;float:none;">
    <fieldset>
    <legend><b>Bitcoin</b></legend>
    <form action="https://zvwapi.appspot.com/store-coinbase.php" method="post" target="_top">
        <table>
        <tr><td><input type="hidden" name="on0" value="Zenvera Points">Zenvera Points</td></tr><tr><td><select name="os0">
                <option value="100 ZP">100 ZP $1.00 USD</option>
                <option value="500 ZP">500 ZP $5.00 USD</option>
                <option value="1100 ZP">1100 ZP $9.99 USD</option>
                <option value="2400 ZP">2400 ZP $20.00 USD</option>
                <option value="6500 ZP">6500 ZP $50.00 USD</option>
        </select> </td></tr>
        <tr><td><input type="hidden" name="on1" value="Account Name">Account Name</td></tr><tr><td><input type="text" name="os1" maxlength="200"></td></tr>
        </table>
        <div align="center">Under Development
        <!--<input type="image" src="https://coinbase.com/assets/buttons/buy_now_small-2161bfbbcfc0444a0c26cdac30778f7a.png" border="0" name="submit" alt="Bitcoin">-->
        </div>
    </form>
    </fieldset>
</div>
<br />
{% endraw %}


__Please double check your account name before placing your order.__
Your items will be available to characters on the account name you provide during checkout as soon as the transaction clears.
You can access the Zenvera redemption system in-game by typing [zenvera at any time or by double-clicking one of the Zenvera stones throughout the world.

Purchased items have no real world value. Due to the nature of the game Zenvera cannot be responsible for nor replace lost or stolen items.

If you require assistance with your order please feel free to e-mail support@zenvera.com.