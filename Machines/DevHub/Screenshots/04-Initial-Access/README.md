# 04 - Initial Access

## Objective
Obtain the first level of access to the target machine by exploiting the identified vulnerability.

## Initial Access
The exploitation of the MCPJam Inspector vulnerability provided an initial foothold as:

- User: `mcp-dev`

## Further Enumeration
During post-exploitation enumeration, a JupyterLab token was discovered.

This token allowed access to JupyterLab under the `analyst` account.

## Arabic Explanation
في هذه المرحلة استغللنا الثغرة التي اكتشفناها في MCPJam Inspector للحصول على وصول أولي بحساب `mcp-dev`.

بعد ذلك، واصلنا الاستكشاف واكتشفنا JupyterLab Token، الذي أتاح لنا الوصول إلى JupyterLab بحساب `analyst`.

## Security Impact
Exposed application functionality and sensitive authentication tokens can provide attackers with unauthorized access to internal services.

## Next Phase
[05 - Privilege Escalation](../05-Privilege-Escalation/)
