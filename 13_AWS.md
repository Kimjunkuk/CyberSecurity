1. "IAM" service - Users & Groups <br>
Global service <br>
Root account created by default <br>
Users<br>
Group only contain users not other groups<br>
Users don't have to belong to group and user can belong to multiple groups.<br>

> 1-1. "IAM" Policies Structure
>> 1-1-1. Consist of 
>>> Version: policy language version, always include "2012-10-17"
>>> Id: an indentifier for the policy (optional)
>>> Statement: one or more individual statements (required)
>> 1-1-2. Statements consists of
>>> Sid: an identifier for the statement (optional)
>>> Effect: whether the statement allows or denies access (Allow, Deny)
>>> Principal: account/user/role to which this policy applied to
>>> Action: list of actions this policy allows or denies
>>> Resource: list of resources to chich the actions applied to
>>> Confition: conditions for when this policy is in effect (optional)
