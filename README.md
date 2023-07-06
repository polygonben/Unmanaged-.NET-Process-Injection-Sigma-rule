# Unmanaged-PowerShell-Sigma-rule
This is a sigma ruleset for detecting unmanaged .NET process injection from Sysmon with Event ID 7 (Image Load) enabled. 

.NET process injection is used as a defence-evasion technqiue by adversaries to run a malicious .NET assembly from within an unmanaged, normal Windows process. This is used by Cobalt Strike's `execute-assembly` function. When process injection occurs, two DLLs - namely `clr.dll` and `clrjit.dll` - are always loaded into the processes memory. Sysmon Event ID 7 can be used to detect this.

This ruleset, or even better the sysmon config,  will need tuning in a production environment to get rid of false-positives.


