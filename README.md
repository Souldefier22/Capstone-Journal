# Capstone-Journal
Individual Notebook

2/2/2022

  Review Project Proposal Template
  Discuss inputs needed for program
  Determine applicable API for program
  General Research on tracing blockchain
  Organization for web page
  
  Take in wallet address and transaction id as inputs
  API could be https://docs.solana.com/developing/clients/javascript-api
  Include a validation step for saving wallet addresses as potential scams
  
  3 pages:
    Input page for bad transaction
    Pathing for finding where the bad transaction leads
    Have seperate page for blacklist of saved wallet addresses
    Profile page for blacklisted addresses
 
  Save how many times a wallet address is reported for people to view
  Possibly add accounts to the applicaion

2/4/2022

  Team Meeting
  Fill out team meeting form
  Make a slide about me for next meeting

  Weekly team meeting form
  Start filling out project proposal

2/7/2022

  Looking through a reported transaction as a basis for tracing the money
  Look at Wormhole incident report
    3 million stolen from wormhole on Solana
  Possibly start tracing when the money has been stolen but hasn't been moved yet
  Start looking at first transaction where they stole money
  Solscan and Solana beach can be helpful tools for tracing
  
  Stretch Goal - add the ability to blacklist wallet addresses
    when an address has been reported 3 times, add it to blacklist address
    find first transaction on address and then go forward from there
    
  Transactions cannot be deleted from blockchain
  Possibly give partial information until they select they would like to see more
  Heroku for web-hosting

  Understanding of how to do a trace from the origin point
  Should go backwards and forwards when given the bad transaction
  Sectioned up the project proposal 
  
2/9/2022

Worked on the Project Proposal 
Came up with tasks for each stage of the project including the front-end, back-end, and blacklist features

2/11/2022

Filled out the project proposal
  Created a Gantt and Pertt chart for the report
    listed the tasks out by weeks for the project
  Filled out itemized budgets
  Filled out safety concerns
  Cpmpleted the economic analysis
Worked on filling out the weekly meeting report

2/14/2022

  Presented Project Proposal
  
2/16/2022

  Setup Jira for backend and user story organization
  Started setting up the environment area by renewing and downloading Pycharm
  Setup a seperate repository for the codebase
  
2/18/2022

  Began setting up development environment
  Created a develepment branch for backend 
  
2/21/2022

  Finished setting up development environment
  Work through a manual trace on the Wormhole attack
  Start working on the backwards tarce manually/focus on functional rather than pretty
  
2/28/2022

  Focus on the traceback for the tranasactions and suspicious accounts
  Possibly switching to the JSON RPC API for getting the transactions on an account
    Solana beach API throwing errors for getting more transactiosn than exist
  Created a loop for going backwards through an account's transactions
  Look at the Long Term Transaction API
  Explore other API

3/2/2022
  
  Looked at alternative API's
  Determined the offset of the solanabeach api couldn't go above 1000 and can't be used
  Resolved first issue of timeout error by switching to genesysgo endpoint for the API
    Loop takes too long to iterate trhough the transactions because only 1000 can be grabbed at a time
    Will still time out but takes longer because there is no limit on the number of API calls
  Met with TA to update them on the ongoing problems with the API's and discuss next steps
  
 3/7/2022
 
  Pivot to a different problem
    Finding the origin of the atacking account is out of scope
    Trace the transactions made by the account and mark them as suspicious
  Be able to mark account that were marked multiple times as suspicious as blacklisted
    Ignore system addresses that will be marked as 11111111111
  Go forward in the trace instead of just backwards
  MVP: Start with an attack transaction, output a list of wallet addresses that are connected to that account and mark them as suspicious 
  
  3/23/2022
  
    The backwards trace is completely functional pending any additional features that come up in the future
      The backwards trace returns a dictionary that has keys for transactions and for accounts where each item is a list of their corresponding values
    Peer Review, Midterm check, and Presentations are completed and turned in
    Possibly implement an API for getting the blacklisted addresses as a stretch goal
      Have an api call for getting the blacklisted and suspicious addresses
      Have an api call for checking whether or not an input address is already marked as suspicious or blacklisted
    Look at mint addresses to see examples of accounts that may not need to be marked
    Start refactoring the tracing code

3/28/2022

  Debugged the backwards trace and forwards trace after refactoring
  Using GenesysGo api for the forwardtrace and quicknode for the backtrace
    Gave an example demonstration of what the end graph design will like
  Start researching how to upload to Heroku
  
3/30/2022

  Started creating files for a gunicorn app
    created Procfile
    created runtime.txt
    created requirements.txt
    created Pipfile
  Still working through errors with pushing to Heroku
  
 4/3/2022
 
  Metup for weekly meeting 
  API calls and re-organized database have been made
  
4/4/2022

  Working on getting a Heroku hosting set up for the project
  Demoed how the graphing works for showing the trace between accounts and transactions
    Showed the progress for both forwards and backwards trace
    Some accounts make transactions that create a loop
  Potentially show the date an account was last made and when the account was created
  Show the first 2 and last 2 characters for the transaction ids and account addresses
    Simplify the frontend look
  3 types of accounts
    -Smart Contract
    -Wallet Addresses
      -check if the assigned id is System Program
    -Data Accounts
      check if the data size is 0
      
4/6/2022

  Added a check for the data based accounts in the backwards trace
    These accounts will now be ignored and not included in final result
  Manually looked through the trace to determine how to look for mint accounts
  Mint variable only establishes what kind of tokens the account holds
    The token accounts may need to be ignored as a whole in order to account for mint accounts
    
4/13/2022

  Working on getting the application hosted
  Refactored the requiremnets file and procfile file
  Updated the backwards trace to ignore data accounts
    only mark normal wallet addresses as suspicious
  
4/18/2022

  Hosting is mostly done, working on getting the database working on the hosting
  The trace no longer records data accounts and mint accounts
  Show what the user just entered and then show the results from there
    Add one more layer
  Add a description that tells people that it has to take a certain amount of time
  Possibly save previous transaction data so that it doesn't have to run in real time 
  
 4/25/2022
 
  Demonstration
  Possibly add a feature for saving previously input transactions
  Possibly add outputs to the frontend as they come in
  
