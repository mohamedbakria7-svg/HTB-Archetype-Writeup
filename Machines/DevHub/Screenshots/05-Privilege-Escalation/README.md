# 05 - Privilege Escalation

## Objective
Escalate privileges from the compromised user to the root account.

## Enumeration Findings
During post-exploitation enumeration, an OPSMCP API key was discovered.

## Exploitation
The `ops._admin_dump` functionality was abused to retrieve sensitive data.

The extracted data included the SSH private key located at:

`/root/.ssh/id_rsa`

## Root Access
The recovered SSH key provided a path to authenticate as the root user.

## Arabic Explanation
بعد الحصول على وصول بحساب `analyst`، واصلنا البحث عن معلومات تساعدنا على تصعيد الصلاحيات.

اكتشفنا مفتاح OPSMCP API، واستفدنا من الدالة `ops._admin_dump` لاستخراج مفتاح SSH الخاص بالمستخدم root، مما أتاح لنا الوصول بصلاحيات المدير الأعلى.

## Security Lessons
- Protect API keys and sensitive credentials.
- Restrict administrative functions.
- Secure private SSH keys and their permissions.

## Next Phase
[06 - Flags](../06-Flags/)
