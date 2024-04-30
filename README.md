<div>
  <h1>Project Title:</h1>
  <p>Verify Account Positions for Client for ACME Systems</p>
</div> 

<div>
  <h1>Summary:</h1>
  <p>This project automates the process of verifying client account positions between ACME System 1 and ACME System 3, aiming to:</p>
  <ul>
    <li>Reduce processing time and improve department performance.</li>
    <li>Maintain data accuracy by comparing account information across systems.</li> 
  </ul>
</div>

<div>
  <h1>Technologies Used:</h1>
  <ul>
    <li>UiPath</li>
    <li>REFramework (Loader + Dispatcher)</li> 
  </ul>
</div>

<div>
  <h1>Workflow:</h1>
  <ol>
    <dt><h4>1️⃣ Initialization</h4></dt>
      <dd>&emsp; ✅ Open the ACME System 1 Web Application</dd>
      <dd>&emsp; ✅ Log in to System 1 (email and password)</dd>
      <dd>&emsp; ✅ Access the Dashboard, it’s the central location where the user can pick a specific menu item</dd>
      <dd>&emsp; ✅ Access the Work Items Listing to consult all the available tasks to perform</dd>
      <dd>&emsp; ✅ Open the ACME System 3 Desktop Application</dd>
      <dd>&emsp; ✅ Log in to ACME System 3 using the same credentials</dd>
    <dt><h4>2️⃣ Loader</h4></dt>
      <dd>&emsp; ✅  The bot loads work items of type "WI1" from ACME System 1 into UiPath Orchestrator.</dd>
    <dt><h4>3️⃣ Dispatcher</h4></dt>
      <dd>&emsp; ✅  The Dispatcher retrieves all work items of type "WI1" for processing.</dd>
    <dt><h4>4️⃣ Processing each work item of type "WI1"</h4></dt>
      <dd>&emsp; ✅  Open the Details page for the selected activity and Read Account Number and Account Amount.</dd>
      <dd>&emsp; ✅  Access the Clients -> Search for Client by Client ID menu option in ACME System 3.</dd>
      <dd>&emsp; ✅  Enter Client based on the ID and double click the Client Name. Also check “Include Inactive Clients” as
sometimes even &emsp;&emsp;&emsp;active clients will not be found otherwise.</dd>
      <dd>&emsp; ✅  Open the Accounts page for the selected client.</dd>
      <dd>&emsp; ✅  Double click the current account based on its number.</dd>
      <dd>&emsp; ✅  Calculate the sum of all transactions for the specified account.</dd>
      <dd>&emsp; ✅  Go back to the Work Item Details and open the “Update Work Item”.</dd>
      <dd>&emsp; ✅  If the sum of all transactions in System 3 is equal to the Account amount in System 1, Set the status to Completed and &emsp;&emsp;&emsp;Add comment: 'Account value matches'.</dd>
  </ol>
</div>
