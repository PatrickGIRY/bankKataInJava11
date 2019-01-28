# bankKataInJava11
Bank kata in Java 11

## Feature: Show account statement
    
As an account holder, I want to show the account statement

### Background: 

* Given an account with a balance of 0
      
### Scenario: Show account statement containing no transaction
        
* When the account holder want to show the account statement
* Then the statement should have the following format:

| DATE | AMOUNT | BALANCE |
| ---- | ------ | ------- |

### Scenario: Show account statement containing a deposit transaction
        
* Given a deposit transaction of 150 on 10-05-2018
* When the account holder want to show the account statement
* Then the statement should have the following format:
            
| DATE       | AMOUNT | BALANCE |
| ---------- | ------ | ------- | 
| 10/05/2018 | 150    | 150     |


### Scenario: Show account statement containing a withdrawal transaction

* Given a withdrawal transaction of 450 on 13-05-2018
* When the account holder want to show the account statement
* Then the statement should have the following format:
  
| DATE       | AMOUNT | BALANCE |
| ---------- | ------ | ------- |
| 10/05/2018 | 150    | -150    |

### Scenario: Show account statement containing several different transactions
        
* Given a deposit transaction of 1000 on 01-07-2018
* And a withdrawal transaction of 100 on 10-07-2018
* And a deposit transaction of 500 on 23-07-2018
* When the account holder want to show the account statement
* Then the statement should have the following format:

| DATE       | AMOUNT  | BALANCE |
| ---------- | ------- | ------- |
| 23/07/2018 | 500.00  | 1400.00 |
| 10/07/2018 | -100.00 | 900.00  |
| 01/07/2018 | 1000.00 | 1000.00 |
