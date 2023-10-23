# How to work:Issue_Postman.
## Step 1 - generate new token
1. Create Api token in yourGitHub profile : <br/>
   Settings -> developer settings -> Personal access token -> Token classics
   2. Turn batton : Generate new token <br/>
   3. Takea a name of key. Assign permission <br/>
   4. Press Batton : Generate token
  
   ---
   ## Step 2 - Postman
   1. Create new Postman collection
   2. Select : Authorization -> Type -> Bearer Token
   3. Input your token from GitHub and save changes
      
  ---
  ## Step 3 - Create Methods
  [General Git Hub Rest Api docs](https://docs.github.com/en/rest/issues/issues?apiVersion=2022-11-28#about-issues)
  ## Get - for get information about issues list <br/>
  https://api.github.com/repos/      {owner}/{repo}/issue <br/>
  ## Post - for create new issues  <br/>
  https://api.github.com/repos/      {owner}/{repo}/issue <br/>
 - Body :<br/>
  {
    "title" : "Issue_1",
    "body" : "Bug Error",
    "assignee" : "Igor-Maltcev",
    "labels" : [
        "bug"
        ] <br/>
        - Script for getting issue number <br/>
        - var key = "issue_number"
var value = pm.response.json().number

pm.collectionVariables.set(key,value);

pm.test("status code is 201", function () {
    pm.response,to.have.status(201);
});
  
  

