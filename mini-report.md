# Mini Report — Redistribute Responsibilities

## Participants
- Pichamon Achirasawad (refactoring)

## Changes
- **`Payroll.py`**: added `change_payroll_date(date, staff_category)` that updates the relevant `PaySchedule` directly.
- **`Bank.py`**: removed `change_payroll_date`, the unused `self.payroll` field, and the `Payroll` import.
- **`client.py`**: now calls `payroll.change_payroll_date()` instead of `bank.change_payroll_date()`. Assertion unchanged.
