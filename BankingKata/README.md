# Bank account kata

## Objectives

Think of your personal bank account experience
When in doubt, go for the simplest solution

## Requirements

- [ ] Deposit and Withdrawal  
- [ ] Transfer  
- [ ] Account statement (date, amount, balance)  
- [ ] Statement printing  
- [ ] Statement filters (just deposits, withdrawal, date)

## BDD

Starting from an acceptance test:

```gherkin
Scenario: Printing statement after deposits and withdrawal
  Given a client makes a deposit of 1000 on 10-01-2012
  And a deposit of 2000 on 13-01-2012
  And a withdrawal of 500 on 14-01-2012
  When she prints her bank statement
  Then she would see
  """
  date       ||   credit ||    debit ||  balance
  14-01-2012 ||          ||   500.00 ||  2500.00
  13-01-2012 ||  2000.00 ||          ||  3000.00
  10-01-2012 ||  1000.00 ||          ||  1000.00
  """
```
