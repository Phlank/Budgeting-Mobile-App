In-line code documentation (SourceCode.md)

In-line Code Documentation
==========================

month.dart
----------

#### Line 45

```
Month build() {
    if (_monthTime == null) throw new NullThrownError();
    if (_income == null) throw new NullThrownError();
    if (_type == null) throw new NullThrownError();
    // Don't need to check if BudgetMaps are null because if they are they can be loaded.
    return new Month._new(
        _monthTime, //
        _income, //
        _type, //
        _allotted, //
        _actual, //
        _transactions);
}
```

Usually in a builder, you need to verify that components are not null for the object to function correctly. However, we don't need all of the budget data and transactions loaded in memory just because we have a reference to the month object. The budget data and transactions will *only* load when they are first requested. It will remain in memory until the app is closed.

### budget.dart

#### Line 86

```
// Makes a new budget based on the allocations of an old budget
  Budget.fromOldBudget(Budget old) {
    _income = old._income;
    _type = old._type;
    _allotted = BudgetMap.copyOf(old._allotted);
    _actual = new BudgetMap();
    _transactions = new TransactionList();
  }
```

This function is used by the PriorityBudgetFactory. There's one crucial part of this function that if done differently would change the behavior of PriorityBudgetFactory completely, and that's the copyOf constructor. Without this, this.\_allotted would be the same object in memory as old.\_allotted.

### steel_crypter.dart

#### Line 14

```
SteelCrypter(Password password) {
    _password = password;
    // Key must be of length 32, but the entered password doesn't need to be.
    // We just use the salt to get to a length of 32.
    String key = _password.secret + _password.salt;
    _aes = new AesCrypt(key, MODE, PADDING);
}
```

SteelCrypt is the library being used here for encryption. It contains an object called AesCrypt, and the key length is required to be 32 bytes long. However, the PIN we require a user to enter is only four characters. Because of that, we adjust the length of the generated salt (created in the password object) such that the length of the user's PIN and the salt combined is 32 bytes.
