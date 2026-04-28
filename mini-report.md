# Mini Report — Redistribute Responsibilities

## Participants
- Pichamon Achirasawad (refactoring)

### Changes
- **`Payroll.py`**: added `change_payroll_date(date, staff_category)` that updates the relevant `PaySchedule` directly.
- **`Bank.py`**: removed `change_payroll_date`, the unused `self.payroll` field, and the `Payroll` import.
- **`client.py`**: now calls `payroll.change_payroll_date()` instead of `bank.change_payroll_date()`. Assertion unchanged.

## Yu, You-Syuan
- There's a god class in the Bank.py file wich include all kind of service, which will cause the problem that all of the function are calling the same class, so i break it down into several different classes seperate by thedifferent function.
- I refactored the God Class by separating different responsibilities into individual service classes. The Bank class now only coordinates these services, so each part of the system can be modified, tested, or fixed independently without affecting the whole project.
