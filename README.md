# Linkedin Bulk Remove Connections
Steps:
1. Go to https://www.linkedin.com/mynetwork/invite-connect/connections/
2. Open Developer Console (Press F12)
3. Go to console and paste this in:

```js
var JQ = $ ;
// for every contact
setInterval( function () {
// this provokes the click on '...'
JQ('[class="artdeco-dropdown__trigger artdeco-dropdown__trigger--placement-bottom ember-view mn-connection-card__dropdown-trigger artdeco-button--tertiary artdeco-button--muted artdeco-button--circle p1"]').click();

// wait on second then provoke a click on "Remove from connections"
setTimeout(function(){ }, 1000);
JQ('button[class="display-flex align-items-center t-14 t-black--light t-normal"]').click(); 

// wait one second
setTimeout(function(){ }, 1000);
JQ('button[class="artdeco-button artdeco-button--2 artdeco-button--primary ember-view artdeco-modal__confirm-dialog-btn"]').click(); 
} , 1000 ) ;
```
