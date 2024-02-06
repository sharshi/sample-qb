Live: https://sharshi-qb-int.azurewebsites.net
Github: https://github.com/sharshi/sample-qb

### The front-end UI should have a button that connects to QuickBooks online and establishes an authentication (store the authentication token in some sort of data storage).

https://sharshi-qb-int.azurewebsites.net/ connect to QB button returns a token as a cookie that can be used to authenticate with QuickBooks.

Unimplemented Improvements: the token is not encripted and is stored in the browser's local storage. It should be stored in a secure way and the token should be refreshed when it expires.

### After authenticating there should be another button that fetches QuickBooks customers and displays it on the screen (also store the data in a data storage)

The previous button redirects to the /Customers page, which is either empty or displays the customers previously fetched from QuickBooks. The data is stored in the browser's `IndexedDB`. When you click `Fetch Customer Info` the data is fetched from QuickBooks and (clears then is) stored in the `IndexedDB` and displayed on the screen.

### Once the data is stored, refreshing the page should pull it from the data store. 
if you refresh the page, the data is pulled from the `IndexedDB` and displayed on the screen. (you can also edit individula items and are synced back to the `IndexedDB`)

### There should now be a new button to refresh the data (which pulls the data from QuickBooks again and overrides the old data in the data store).

The `Fetch Customer Info` button fetches the data from QuickBooks and overrides the old data in the `IndexedDB`.

See the data updating in the `IndexedDB` in the browser's dev tools.

### Technical Details
.Net 8
Azure App Service for hosting
App Config for configuration
IndexedDB for local storage