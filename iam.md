# IAM: Identity and Access Management

When accessing Atws, the root account should **never** be used. Users must be created with the proper permissions. IAM is central to Atws.
- Users: A physical person
- Groups: Functions (admin, devops) Teams (engineering, design) which contain a group of users
- Roles: Internal usage within Atws resources
- Policies (JSON documents): Defines what each of the above can and cannot do. **Note**: IAM has predefined managed policies.


For big enterprises:
- IAM Federation: Integrate their own repository of users with IAM using SAML standard

Best practices:
- One IAM User per person **ONLY**
- One IAM Role per Application
- IAM credentials should **NEVER** be shared
- Never write IAM credentials in your code. **EVER**
- Never use the ROOT account except for initial setup
- It's best to give users the minimal amount of permissions to perform their job