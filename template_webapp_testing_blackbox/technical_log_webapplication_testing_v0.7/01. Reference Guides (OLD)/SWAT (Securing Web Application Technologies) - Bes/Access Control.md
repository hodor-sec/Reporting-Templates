
| Best Practice | Description | CWE ID |
| --- | --- | --- |
| Apply Access Controls Checks Consistently | Always apply the principle of complete mediation, forcing all requeststhrough a common security "gate keeper." This ensures that access control checks are triggered whether or not the user is authenticated. | cwe-284 |
| Apply the Principle of Least Privilege | Make use of a Mandatory Access Control system. All access decisions will be based on the principle of least privilege. If not explicitly allowed then access should be denied. Additionally, after an account is created,rights must be specifically added to that account to grant access to resources. | cwe-272<br>cwe-250 |
| Don't Use Direct Object References for Access Control Checks | Do not allow direct references to files or parameters that can be manipulated to grant excessive access. Access control decisions must be based on the authenticated user identity and trusted server side information. | cwe-284 |
| Don't Use Unvalidated Forwards or Redirects | An unvalidated forward can allow an attacker to access private content without authentication. Unvalidated redirects allow an attacker to lure victims into visiting malicious sites. Prevent these from occurring by conducting the appropriate access controls checks before sending the user to the given location. | cwe-601 |

