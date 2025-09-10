#NX Witness can interface to Zenitel Connect Pro using REST.

A Node-RED flow is required to handle authentication updates of the bearer tokens for both ZCP and NX Witness.
NX Witness events can then be used to trigger events in ZCP using the REST interface.

Note: The process runs every 80 seconds, so additions and changes within NX may not work immediately, but will propagate over the next 80 seconds.
This can be sped up by restarting the Node-RED flow.

It's assumed that you have already created a Zenitel Link account in Zenitel Connect Pro for integration and you have a working NX Witness VMS.

Import the Node-RED flow into Node-RED. Edit the Setup Details node and update with the required settings

Connect Pro IP Address
Connect Pro Zenitel Link Username
Connect Pro Zenitel Link Password
NX Witness IP Address
NX Witness Username
NX Witness Password

Deploy the flow and it will obtain the bearer tokens and begin scraping the NX Witness Events for the word Zenitel anywhere in the Title.
