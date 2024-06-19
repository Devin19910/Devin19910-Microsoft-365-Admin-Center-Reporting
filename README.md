# Devin19910-Microsoft-365-Admin-Center-Reporting
PowerShell scripts to generate reports from Microsoft 365 Admin Center. These reports can provide insights into user activity, license usage, and security compliance.

Project Outline:
•	README.MD: Explanation of the reporting scripts and how to run them.
•	Scripts:
o	UserActivityReport.ps1: Script to generate a report on user activity.
o	LicenseUsageReport.ps1: Script to generate a report on license usage.
o	SecurityComplianceReport.ps1: Script to generate a report on security compliance.


Example Code Snippet (UserActivityReport.ps1):

# Connect to MS Graph API
Connect-MSGraph

# Generate user activity report
$userActivity = Get-MgAuditLogSignIn -Filter "createdDateTime ge 2023-01-01 and createdDateTime le 2023-12-31"

# Export report to CSV
$userActivity | Export-Csv -Path "UserActivityReport.csv" -NoTypeInformation

Write-Output "User activity report generated: UserActivityReport.csv"
