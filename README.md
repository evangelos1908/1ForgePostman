# 1ForgePostman

There are two ways to run the 1ForgeAPI collection.
The first one is through the Collection runner by using the forex_dataset.csv file.
The second one is to directly send the API call and to validate particular pair(s).

The two examples below illustrate the solution

------------------------------------------------------
Using the .csv file and perform more than 1 iterations
------------------------------------------------------
1. Import the 1ForgeAPI.postman_collection.json collection
2. Import the 1forge.postman_environment.json environment
3. Add your API_KEY in the APIKey enviroment variable
4. Open the collection runner
5. Select the proper environment
6. Import the forex_dataset.csv file in the Data field
7. Set a number of iterations

The collection will be executed as many times as the value of the iterations field. 
Each time a different pair of currency will be passed.

----------------------------------------------------
Send an API call without using the Collection Runner
----------------------------------------------------
This way is used when a particular pair of currency is required to be tested
1. Import the 1ForgeAPI.postman_collection.json collection
2. Import the 1forge.postman_environment.json environment
3. Add your API_KEY in the APIKey enviroment variable
4. Add the pair you want to test in the quote enviroment variable (current value)
5. Add the expected results in the enviroment variable with the same name as the pair sent
i.e. if AUDUSD is sent, then:
VARIABLE: AUDUSD
CURRENT VALUE = {
        "symbol": "AUDUSD"
                }
                
                
