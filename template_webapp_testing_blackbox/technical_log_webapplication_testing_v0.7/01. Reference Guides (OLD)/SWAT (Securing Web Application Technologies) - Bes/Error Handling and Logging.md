
| Best Practice | Description | CWE ID |
| --- | --- | --- |
| Display Generic Error Messages | Error messages should not reveal details about the internal state of the application. For example, file system path and stack information should not be exposed to the user through error messages. | cwe-209 |
| No Unhandled Exceptions | Given the languages and frameworks in use for web application development, never allow an unhandled exception to occur. Error handlers should be configured to handle unexpected errors and gracefully return controlled output to the user. | cwe-391 |
| Suppress Framework Generated Errors | Your development framework or platform may generate default error messages. These should be suppressed or replaced with customized error messages as framework generated messages may reveal sensitive information to the user. | cwe-209 |
| Log All Authentication Activities | Any authentication activities, whether successful or not, should be logged. | cwe-778 |
| Log All Privilege Changes | Any activities or occasions where the user's privilege level changes should be logged. | cwe-778 |
| Log Administrative Activities | Any administrative activities on the application or any of its components should be logged. | cwe-778 |
| Log Access to Sensitive Data | Any access to sensitive data should be logged. This is particularly important for corporations that have to meet regulatory requirements like HIPAA, PCI, or SOX. | cwe-778 |
| Do Not Log Inappropriate Data | While logging errors and auditing access is important, sensitive data should never be logged in an unencrypted form. For example, under HIPAA and PCI, it would be a violation to log sensitive data into the log itself unless the log is encrypted on the disk. Additionally, it can create a serious exposure point should the web application itself become compromised. | cwe-532 |
| Store Logs Securely | Logs should be stored and maintained appropriately to avoid information loss or tampering by intruder. Log retention shouldalso follow the retention policy set forth by the organization to meet regulatory requirements and provide enough information for forensic and incident response activities. | cwe-533 |

