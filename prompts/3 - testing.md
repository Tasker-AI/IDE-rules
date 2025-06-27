# Testing Prompt

```md
We are currently in stage <X> and have recently implemented the changes in `checklist.md`

I want to make sure everything works properly.
Please conduct a simple set of tests, either by creating a testing script or simply by testing API routes and backend features via your terminal.

I am looking for the simplest, most straightforward confirmation that everything works. We are building an MVP here, not Google core infrastructure.

Execute the tests right away, and report back to me with any issues.
```

# Testing Prompt 2

```md
1. Write tests first (TDD) when possible
2. Test public interfaces, not implementation details
3. Use meaningful test names that describe the scenario
4. Keep tests independent and isolated
5. Test edge cases and error conditions

Example:
def test_withdraw_insufficient_funds():
    account = BankAccount()
    account.deposit(100)
    
    with pytest.raises(InsufficientFunds):
        account.withdraw(150)
```