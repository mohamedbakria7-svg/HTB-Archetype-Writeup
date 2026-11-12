# 06 - Flags

## Objective
Document the successful completion of the DevHub machine.

## User Flag
- File: `/home/analyst/user.txt`
- Account: `analyst`

## Root Flag
- File: `/root/root.txt`
- Account: `root`

## Completion Summary
The machine was completed by:
1. Enumerating exposed services.
2. Identifying the MCPJam Inspector vulnerability.
3. Obtaining initial access as `mcp-dev`.
4. Accessing JupyterLab as `analyst`.
5. Abusing the OPSMCP administrative functionality.
6. Recovering the root SSH private key and obtaining root access.

## Arabic Explanation
في هذه المرحلة نوثق نجاح الوصول إلى حساب analyst للحصول على User Flag، ثم الوصول إلى root للحصول على Root Flag.

**Note:** The actual flag values are intentionally not included in this public writeup.

## Conclusion
DevHub demonstrated the importance of securing exposed MCP services, API keys, administrative functions, and SSH private keys.
