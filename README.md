# ba_warsaw
25.02 there is and API workshop.
Yulia presents a BROKER, so API requests and repsonses provide JSONS for this role according to USE-CASE described below.
https://docs.google.com/document/d/1c4HLmuQ5NG3zmjt7zQyDdG5ITVZbPI0judACYXS2rvc/edit#



BR-API-1: Retrieve Policies under a Broker
BR-API-2: Add Policy to an Employer

Pre-conditions:
User (Broker) is logged in

Main flow:
1.User opens a list of available Policies
2.System loads a list of current Policies associated with a Broker (call BR-API-1)
   -25 items per page
   -Display a total number of results
   -Sorted by Effective date
   -List attributes
     --Policy type
     --Effective Date
     --Holder name (Employee name)
     --Employer name
     --Amount
     --Frequency
3.User selects an option to assign a new Policy
4.System displays a page to add a Policy
5.User selects an Organization
6.User selects an Employee
7.User provides the Policy detail
  -Policy type
  -Policy amount
  -Effective date
  -Coverages
8.User triggers policy submission
9.System submits the new Policy (call BR-API-2)
