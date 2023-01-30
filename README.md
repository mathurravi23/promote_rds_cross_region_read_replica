# promote_rds_cross_region_read_replica



Create your Lambda function with the following parameters:

HOSTED_ZONE_ID           : ID of Route53 private hosted zone. It store CNAME enteris for RDS SQL Server endpoints.
PRIMARY_DB_IDENTIFIER    : RDS Instance identifier of primary RDS SQL Server instance in primary AWS region.
PRIMARY_REGION           : Primary AWS region. e.g. us-east-1
REPLICA_DB_IDENTIFIER.   : RDS Instance identifier of RDS SQL Server cross region read replica.
SECONDARY_REGION         : Secondary AWS region. e.g. us-east-2
ACCEPTABLE_RR_LAG_SECONDS: Set this parameter to a numeric value (in seconds). If replica lag is greater than this value, Lambda function will not initiate cross region read replica promotion and you can manually perform the steps.
