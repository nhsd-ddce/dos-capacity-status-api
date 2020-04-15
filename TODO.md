# TODO

## Priority list

- Testing
  - Create a test user from a script that can be easily executed, configured and customised
- Application
  - Protect proxy `/admin` endpoint (CSAPI-62)
  - Add logging in a format that can be picked up by existing DoS Splunk (CSAPI-7)
  - Increase the max reset status period in mins to 5 hours (CSAPI-63)
  - PUT vs. PATCH
- Development
  - Consistent formatting in IDE and command-line (flake8)
- Development
  - Consistent formatting in IDE and command-line (flake8)
- Documentation
  - Generate API Documentation automatically (CSAPI-9)
- Testing
  - Check for unit and integration test completeness (CSAPI-64)
  - Can unit and integration tests be run independently
  - Implement smoke test suite

### Other tasks

- Security
  - Create a new DoS user only to be used by the API application
  - API request throttling
- Application
  - Let's revisit the domain model and consider again the naming of `serviceUid`, `serviceName`, `capacityStatus`
- Infrastructure
  - Split DB responsibility, DoS DB should run a container and API connects to it's own RDS
  - Change RDS DB identifier, currently it is `uec-dos-api-cs-nonprod-db`
  - Change RDS Security Group, currently it is `uec-dos-api-cs-nonprod-db-sg`
  - Move RDS Terraform variables to Make profile
  - Sort out tags
  - Create [custom option group](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithOptionGroups.html) for the RDS instance
  - Move RDS password to the `uec-dos-api-capacity-status-$(PROFILE)` secret
  - Review Subnet Group
  - Review Security Group rule
  - Refactor RDS configuration
  - Refactor ALB and WAF configuration
  - Refactor Kubernetes deployment scripts
  - Crete Route 53 record automatically (CSAPI-55)
  - Create Secrets Manager entry automatically
  - API throttling (CSAPI-44)
  - Database backup and restore scripts
- Documentation
  - Generate API Documentation automatically (CSAPI-9)
- Testing
  - Provide acceptance test suite
  - Provide load test suite
  - Provide security test suite
- Deployment
  - Deploy to production (CSAPI-65, CSAPI-66)
  - Implement Jenkins pipeline (CSAPI-65, CSAPI-66)
  - Tagging upon deployment (CSAPI-65, CSAPI-66)
- Monitoring:
  - Configure Splunk (CSAPI-70)
  - Configure Instana (CSAPI-69)
  - Configure Pingdom
  - Configure CloudWatch
  - Configure Slack