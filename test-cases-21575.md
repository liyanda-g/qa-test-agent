🟢 Test Case 1 — Successful Lease Creation

Preconditions:

User logged in as Leasing Officer
Property and unit available

Steps:

Navigate to Lease Module
Enter valid tenant details
Select property and unit
Enter valid start date and end date
Enter rent amount
Click Submit

Expected Result:

Lease is created successfully
Status moves to “Pending Approval”
🟢 Test Case 2 — Mandatory Field Validation

Steps:

Navigate to Lease Module
Leave required fields empty (tenant, unit, rent)
Click Submit

Expected Result:

System should display validation errors
Lease should NOT be created
🟢 Test Case 3 — Start Date Greater Than End Date

Steps:

Enter lease start date = 10/10/2026
Enter lease end date = 05/10/2026
Submit

Expected Result:

Error message displayed
“Start date cannot be greater than end date”
🟢 Test Case 4 — Past Date Validation

Steps:

Enter lease start date in the past
Fill remaining valid data
Submit

Expected Result:

System should prevent submission OR show warning
🟢 Test Case 5 — Lease Without Tenant

Steps:

Leave tenant field empty
Fill all other fields
Submit

Expected Result:

Error: “Tenant details are required”
🟢 Test Case 6 — Rent Calculation Validation

Steps:

Enter rent amount = negative value OR 0
Submit

Expected Result:

System should reject invalid rent
Error message displayed
🟢 Test Case 7 — Multiple Tenants / Roommates

Steps:

Add multiple tenants
Submit lease

Expected Result:

All tenants appear in lease
Data saved correctly
🟢 Test Case 8 — Co-signer Validation

Steps:

Add co-signer without tenant
Submit

Expected Result:

System should NOT allow lease without tenant
Co-signer alone is invalid
🟢 Test Case 9 — Lease Approval Flow

Steps:

Create lease
Submit for approval
Login as approver
Approve lease

Expected Result:

Lease status changes to “Active”
