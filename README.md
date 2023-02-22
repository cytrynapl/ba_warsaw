# ba_warsaw_broker
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


Alternative flows:
   2a. No current Policies associated with a Broker
      1.System displays a message “No current Policies”
   2b. User filters Policy list
      1.User applies one of the filters: Policy type, Holder name, Employer name, Frequency
      2.System filters the list based on provide criteria 
   4a. No current Employers for a Holder
      1.Return message “No current employment”
      2.Go to step 2

Post-conditions:
-A new Policy is created
-System calculates a commision and assign it to the Policy
-The Policy is available in the Policies list

