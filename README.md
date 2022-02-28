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
