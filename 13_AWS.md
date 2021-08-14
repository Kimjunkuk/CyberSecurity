1. "IAM" service - Users & Groups <br>
Global service <br>
Root account created by default <br>
Users<br>
Group only contain users not other groups<br>
Users don't have to belong to group and user can belong to multiple groups.<br>

> 1-1. "IAM" Policies Structure
>> 1-1-1. Consist of 
>>> 1-1-1-1. Version: policy language version, always include "2012-10-17" <br>
>>> 1-1-1-2. Id: an indentifier for the policy (optional) <br>
>>> 1-1-1-3. Statement: one or more individual statements (required) <br>
>> 1-1-2. Statements consists of <br>
>>> 1-1-2-1. Sid: an identifier for the statement (optional) <br>
>>> 1-1-2-2. Effect: whether the statement allows or denies access (Allow, Deny) <br>
>>> 1-1-2-3. Principal: account/user/role to which this policy applied to <br>
>>> 1-1-2-4. Action: list of actions this policy allows or denies <br>
>>> 1-1-2-5. Resource: list of resources to chich the actions applied to <br>
>>> 1-1-2-6. Confition: conditions for when this policy is in effect (optional) <br>
