## 1.7.3 (Unreleased)
## 1.7.2 (February 09, 2018)

IMPROVEMENTS:

- *New DataSource*: _alicloud_eips_ ([#110](https://github.com/terraform-providers/terraform-provider-alicloud/pull/110))
- *New DataSource*: _alicloud_vswitches_ ([#109](https://github.com/terraform-providers/terraform-provider-alicloud/pull/109))
- Support inner network segregation in one security group ([#112](https://github.com/terraform-providers/terraform-provider-alicloud/pull/112))

BUG FIXES:

- Fix creating Classic instance failed result in role_name ([#111](https://github.com/terraform-providers/terraform-provider-alicloud/pull/111))
- Fix eip is not exist in nat gateway when creating snat ([#108](https://github.com/terraform-providers/terraform-provider-alicloud/pull/108))

## 1.7.1 (February 02, 2018)

IMPROVEMENTS:

- Support setting instance_name for ESS scaling configuration ([#107](https://github.com/terraform-providers/terraform-provider-alicloud/pull/107))
- Support multiple vswitches for ESS scaling group and output slbIds and dbIds ([#105](https://github.com/terraform-providers/terraform-provider-alicloud/pull/105))
- Support to set internet_max_bandwidth_out is 0 for ESS configuration ([#103](https://github.com/terraform-providers/terraform-provider-alicloud/pull/103))
- Modify EIP default to PayByTraffic for international account ([#101](https://github.com/terraform-providers/terraform-provider-alicloud/pull/101))
- Deprecate nat gateway fileds 'spec' and 'bandwidth_packages' ([#100](https://github.com/terraform-providers/terraform-provider-alicloud/pull/100))
- Support to associate EIP with SLB and Nat Gateway ([#99](https://github.com/terraform-providers/terraform-provider-alicloud/pull/99))

BUG FIXES:

- fix a bug that can't create multiple VPC, vswitch and nat gateway at one time ([#102](https://github.com/terraform-providers/terraform-provider-alicloud/pull/102))
- fix a bug that can't import instance 'role_name' ([#104](https://github.com/terraform-providers/terraform-provider-alicloud/pull/104))
- fix a bug that creating ESS scaling group and configuration results from 'Throttling' ([#106](https://github.com/terraform-providers/terraform-provider-alicloud/pull/106))

## 1.7.0 (January 25, 2018)

IMPROVEMENTS:

- *New Resource*: _alicloud_kms_key_ ([#91](https://github.com/terraform-providers/terraform-provider-alicloud/pull/91))
- *New DataSource*: _alicloud_kms_keys_ ([#93](https://github.com/terraform-providers/terraform-provider-alicloud/pull/93))
- *New DataSource*: _alicloud_instances_ ([#94](https://github.com/terraform-providers/terraform-provider-alicloud/pull/94))
- Add a new output field "arn" for _alicloud_kms_key_ ([#92](https://github.com/terraform-providers/terraform-provider-alicloud/pull/92))
- Add a new field "specification" for _alicloud_slb_ ([#95](https://github.com/terraform-providers/terraform-provider-alicloud/pull/95))
- Improve security group rule's port range for "-1/-1" ([#96](https://github.com/terraform-providers/terraform-provider-alicloud/pull/96))

BUG FIXES:

- fix slb invalid status error when launching ESS scaling group ([#97](https://github.com/terraform-providers/terraform-provider-alicloud/pull/97))

## 1.6.2 (January 22, 2018)

IMPROVEMENTS:

- Modify db_connection prefix default value to "instance_id + 'tf'"([#90](https://github.com/terraform-providers/terraform-provider-alicloud/pull/90))
- Modify db_connection ID to make it more simple while importing it([#90](https://github.com/terraform-providers/terraform-provider-alicloud/pull/90))
- Add wait method to avoid useless status error while creating/modifying account or privilege or connection or database([#90](https://github.com/terraform-providers/terraform-provider-alicloud/pull/90))
- Support to set instnace name for RDS ([#88](https://github.com/terraform-providers/terraform-provider-alicloud/pull/88))
- Avoid container cluster cidr block conflicts with vswitch's ([#88](https://github.com/terraform-providers/terraform-provider-alicloud/pull/88))
- Output resource import information ([#87](https://github.com/terraform-providers/terraform-provider-alicloud/pull/87))

BUG FIXES:

- fix instance id not found and instane status not supported bug([#90](https://github.com/terraform-providers/terraform-provider-alicloud/pull/90))
- fix deleting slb_attachment resource failed bug ([#86](https://github.com/terraform-providers/terraform-provider-alicloud/pull/86))


## 1.6.1 (January 18, 2018)

IMPROVEMENTS:

- Support to modify instance type and network spec ([#84](https://github.com/terraform-providers/terraform-provider-alicloud/pull/84))
- Avoid needless error when creating security group rule ([#83](https://github.com/terraform-providers/terraform-provider-alicloud/pull/83))

BUG FIXES:

- fix creating cluster container failed bug ([#85](https://github.com/terraform-providers/terraform-provider-alicloud/pull/85))


## 1.6.0 (January 15, 2018)

IMPROVEMENTS:

- *New Resource*: _alicloud_ess_attachment_ ([#80](https://github.com/terraform-providers/terraform-provider-alicloud/pull/80))
- *New Resource*: _alicloud_slb_rule_ ([#79](https://github.com/terraform-providers/terraform-provider-alicloud/pull/79))
- *New Resource*: _alicloud_slb_server_group_ ([#78](https://github.com/terraform-providers/terraform-provider-alicloud/pull/78))
- Support Spot Instance ([#77](https://github.com/terraform-providers/terraform-provider-alicloud/pull/77))
- Output tip message when international account create SLB failed ([#75](https://github.com/terraform-providers/terraform-provider-alicloud/pull/75))
- Standardize the order of imports packages ([#74](https://github.com/terraform-providers/terraform-provider-alicloud/pull/74))
- Add "weight" for slb_attachment to improve the resource ([#81](https://github.com/terraform-providers/terraform-provider-alicloud/pull/81))

BUG FIXES:

- fix allocating RDS public connection conflict error ([#76](https://github.com/terraform-providers/terraform-provider-alicloud/pull/76))

## 1.5.3 (January 9, 2018)

BUG FIXES:
  * fix getting OSS endpoint failed error  ([#73](https://github.com/terraform-providers/terraform-provider-alicloud/pull/73))
  * fix describing dns record not found when deleting record ([#73](https://github.com/terraform-providers/terraform-provider-alicloud/pull/73))

## 1.5.2 (January 8, 2018)

BUG FIXES:
  * fix creating rds 'Prepaid' instance failed error  ([#70](https://github.com/terraform-providers/terraform-provider-alicloud/pull/70))

## 1.5.1 (January 5, 2018)

BUG FIXES:
  * modify security_token to Optional ([#69](https://github.com/terraform-providers/terraform-provider-alicloud/pull/69))

## 1.5.0 (January 4, 2018)

IMPROVEMENTS:

- *New Resource*: _alicloud_db_database_ ([#68](https://github.com/terraform-providers/terraform-provider-alicloud/pull/68))
- *New Resource*: _alicloud_db_backup_policy_ ([#68](https://github.com/terraform-providers/terraform-provider-alicloud/pull/68))
- *New Resource*: _alicloud_db_connection_ ([#67](https://github.com/terraform-providers/terraform-provider-alicloud/pull/67))
- *New Resource*: _alicloud_db_account_ ([#66](https://github.com/terraform-providers/terraform-provider-alicloud/pull/66))
- *New Resource*: _alicloud_db_account_privilege_ ([#66](https://github.com/terraform-providers/terraform-provider-alicloud/pull/66))
- resource/db_instance: remove some field to new resource ([#65](https://github.com/terraform-providers/terraform-provider-alicloud/pull/65))
- resource/instance: support to modify private ip, vswitch_id and instance charge type ([#65](https://github.com/terraform-providers/terraform-provider-alicloud/pull/65))

BUG FIXES:

- resource/dns-record: Fix dns record still exist after deleting it ([#65](https://github.com/terraform-providers/terraform-provider-alicloud/pull/65))
- resource/instance: fix deleting route entry error ([#69](https://github.com/terraform-providers/terraform-provider-alicloud/pull/69))


## 1.2.0 (December 15, 2017)

IMPROVEMENTS:
- resource/slb: wait for SLB active before return back ([#61](https://github.com/terraform-providers/terraform-provider-alicloud/pull/61))

BUG FIXES:

- resource/dns-record: Fix setting dns priority failed ([#58](https://github.com/terraform-providers/terraform-provider-alicloud/pull/58))
- resource/dns-record: Fix ESS attachs SLB failed ([#59](https://github.com/terraform-providers/terraform-provider-alicloud/pull/59))
- resource/dns-record: Fix security group not found error ([#59](https://github.com/terraform-providers/terraform-provider-alicloud/pull/59))


## 1.0.0 (December 11, 2017)

IMPROVEMENTS:

- *New Resource*: _alicloud_slb_listener_ ([#53](https://github.com/terraform-providers/terraform-provider-alicloud/pull/53))
- *New Resource*: _alicloud_cdn_domain_ ([#52](https://github.com/terraform-providers/terraform-provider-alicloud/pull/52))
- *New Resource*: _alicloud_dns_ ([#51](https://github.com/terraform-providers/terraform-provider-alicloud/pull/51))
- *New Resource*: _alicloud_dns_group_ ([#51](https://github.com/terraform-providers/terraform-provider-alicloud/pull/51))
- *New Resource*: _alicloud_dns_record_ ([#51](https://github.com/terraform-providers/terraform-provider-alicloud/pull/51))
- *New Resource*: _alicloud_ram_account_alias_ ([#50](https://github.com/terraform-providers/terraform-provider-alicloud/pull/50))
- *New Resource*: _alicloud_ram_login_profile_ ([#50](https://github.com/terraform-providers/terraform-provider-alicloud/pull/50))
- *New Resource*: _alicloud_ram_access_key_ ([#50](https://github.com/terraform-providers/terraform-provider-alicloud/pull/50))
- *New Resource*: _alicloud_ram_group_ ([#49](https://github.com/terraform-providers/terraform-provider-alicloud/pull/49))
- *New Resource*: _alicloud_ram_group_membership_ ([#49](https://github.com/terraform-providers/terraform-provider-alicloud/pull/49))
- *New Resource*: _alicloud_ram_group_policy_attachment_ ([#49](https://github.com/terraform-providers/terraform-provider-alicloud/pull/49))
- *New Resource*: _alicloud_ram_role_ ([#48](https://github.com/terraform-providers/terraform-provider-alicloud/pull/48))
- *New Resource*: _alicloud_ram_role_attachment_ ([#48](https://github.com/terraform-providers/terraform-provider-alicloud/pull/48))
- *New Resource*: _alicloud_ram_role_polocy_attachment_ ([#48](https://github.com/terraform-providers/terraform-provider-alicloud/pull/48))
- *New Resource*: _alicloud_container_cluster_ ([#47](https://github.com/terraform-providers/terraform-provider-alicloud/pull/47))
- *New Resource:* _alicloud_ram_policy_ ([#46](https://github.com/terraform-providers/terraform-provider-alicloud/pull/46))
- *New Resource*: _alicloud_ram_user_policy_attachment_ ([#46](https://github.com/terraform-providers/terraform-provider-alicloud/pull/46))
- *New Resource* _alicloud_ram_user_ ([#44](https://github.com/terraform-providers/terraform-provider-alicloud/pull/44))
- *New Datasource* _alicloud_ram_policies_ ([#46](https://github.com/terraform-providers/terraform-provider-alicloud/pull/46))
- *New Datasource* _alicloud_ram_users_ ([#44](https://github.com/terraform-providers/terraform-provider-alicloud/pull/44))
- *New Datasource*: _alicloud_ram_roles_ ([#48](https://github.com/terraform-providers/terraform-provider-alicloud/pull/48))
- *New Datasource*: _alicloud_ram_account_aliases_ ([#50](https://github.com/terraform-providers/terraform-provider-alicloud/pull/50))
- *New Datasource*: _alicloud_dns_domains_ ([#51](https://github.com/terraform-providers/terraform-provider-alicloud/pull/51))
- *New Datasource*: _alicloud_dns_groups_ ([#51](https://github.com/terraform-providers/terraform-provider-alicloud/pull/51))
- *New Datasource*: _alicloud_dns_records_ ([#51](https://github.com/terraform-providers/terraform-provider-alicloud/pull/51))
- resource/instance: add new parameter `role_name` ([#48](https://github.com/terraform-providers/terraform-provider-alicloud/pull/48))
- resource/slb: remove slb schema field `listeners` and using new listener resource to replace ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
- resource/ess_scaling_configuration: add new parameters `key_name`, `role_name`, `user_data`, `force_delete` and `tags` ([#54](https://github.com/terraform-providers/terraform-provider-alicloud/pull/54))
- resource/ess_scaling_configuration: remove it importing ([#54](https://github.com/terraform-providers/terraform-provider-alicloud/pull/54))
- resource: format not found error ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
- website: improve resource docs ([#56](https://github.com/terraform-providers/terraform-provider-alicloud/pull/56))
- examples: add new examples, like oss, key_pair, router_interface and so on ([#56](https://github.com/terraform-providers/terraform-provider-alicloud/pull/56))

- Added support for importing:
  - `alicloud_container_cluster` ([#47](https://github.com/terraform-providers/terraform-provider-alicloud/pull/47))
  - `alicloud_ram_policy` ([#46](https://github.com/terraform-providers/terraform-provider-alicloud/pull/46))
  - `alicloud_ram_user` ([#44](https://github.com/terraform-providers/terraform-provider-alicloud/pull/44))
  - `alicloud_ram_role` ([#48](https://github.com/terraform-providers/terraform-provider-alicloud/pull/48))
  - `alicloud_ram_groups` ([#49](https://github.com/terraform-providers/terraform-provider-alicloud/pull/49))
  - `alicloud_ram_login_profile` ([#50](https://github.com/terraform-providers/terraform-provider-alicloud/pull/50))
  - `alicloud_dns` ([#51](https://github.com/terraform-providers/terraform-provider-alicloud/pull/51))
  - `alicloud_dns_record` ([#51](https://github.com/terraform-providers/terraform-provider-alicloud/pull/51))
  - `alicloud_slb_listener` ([#53](https://github.com/terraform-providers/terraform-provider-alicloud/pull/53))
  - `alicloud_security_group` ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
  - `alicloud_slb` ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
  - `alicloud_vswitch` ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
  - `alicloud_vroute_entry` ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))

BUG FIXES:

- resource/vroute_entry: Fix building route_entry concurrency issue ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
- resource/vswitch: Fix building vswitch concurrency issue ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
- resource/router_interface: Fix building router interface concurrency issue ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
- resource/vpc: Fix building vpc concurrency issue ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))
- resource/slb_attachment: Fix attaching slb failed ([#55](https://github.com/terraform-providers/terraform-provider-alicloud/pull/55))

## 0.1.1 (December 11, 2017)

IMPROVEMENTS:

- *New Resource:* _alicloud_key_pair_ ([#27](https://github.com/terraform-providers/terraform-provider-alicloud/pull/27))
- *New Resource*: _alicloud_key_pair_attachment_ ([#28](https://github.com/terraform-providers/terraform-provider-alicloud/pull/28))
- *New Resource*: _alicloud_router_interface_ ([#40](https://github.com/terraform-providers/terraform-provider-alicloud/pull/40))
- *New Resource:* _alicloud_oss_bucket_ ([#10](https://github.com/terraform-providers/terraform-provider-alicloud/pull/10))
- *New Resource*: _alicloud_oss_bucket_object_ ([#14](https://github.com/terraform-providers/terraform-provider-alicloud/pull/14))
- *New Datasource* _alicloud_key_pairs_ ([#30](https://github.com/terraform-providers/terraform-provider-alicloud/pull/30))
- *New Datasource* _alicloud_vpcs_ ([#34](https://github.com/terraform-providers/terraform-provider-alicloud/pull/34))
- *New output_file* option for data sources: export data to a specified file ([#29](https://github.com/terraform-providers/terraform-provider-alicloud/pull/29))
- resource/instance:add new parameter `key_name` ([#31](https://github.com/terraform-providers/terraform-provider-alicloud/pull/31))
- resource/route_entry: new nexthop type 'RouterInterface' for route entry ([#41](https://github.com/terraform-providers/terraform-provider-alicloud/pull/41))
- resource/security_group_rule: Remove `cidr_ip` contribute "ConflictsWith" ([#39](https://github.com/terraform-providers/terraform-provider-alicloud/pull/39))
- resource/rds: add ability to change instance password ([#17](https://github.com/terraform-providers/terraform-provider-alicloud/pull/17))
- resource/rds: Add ability to import existing RDS resources ([#16](https://github.com/terraform-providers/terraform-provider-alicloud/pull/16))
- datasource/alicloud_zones: Add more options for filtering ([#19](https://github.com/terraform-providers/terraform-provider-alicloud/pull/19))
- Added support for importing:
  - `alicloud_vpc` ([#32](https://github.com/terraform-providers/terraform-provider-alicloud/pull/32))
  - `alicloud_route_entry` ([#33](https://github.com/terraform-providers/terraform-provider-alicloud/pull/33))
  - `alicloud_nat_gateway` ([#26](https://github.com/terraform-providers/terraform-provider-alicloud/pull/26))
  - `alicloud_ess_schedule` ([#25](https://github.com/terraform-providers/terraform-provider-alicloud/pull/25))
  - `alicloud_ess_scaling_group` ([#24](https://github.com/terraform-providers/terraform-provider-alicloud/pull/24))
  - `alicloud_instance` ([#23](https://github.com/terraform-providers/terraform-provider-alicloud/pull/23))
  - `alicloud_eip` ([#22](https://github.com/terraform-providers/terraform-provider-alicloud/pull/22))
  - `alicloud_disk` ([#21](https://github.com/terraform-providers/terraform-provider-alicloud/pull/21))

BUG FIXES:

- resource/disk_attachment: Fix issue attaching multiple disks and set disk_attachment's parameter 'device_name' as deprecated ([#9](https://github.com/terraform-providers/terraform-provider-alicloud/pull/9))
- resource/rds: Fix diff error about rds security_ips ([#13](https://github.com/terraform-providers/terraform-provider-alicloud/pull/13))
- resource/security_group_rule: Fix diff error when authorizing security group rules ([#15](https://github.com/terraform-providers/terraform-provider-alicloud/pull/15))
- resource/security_group_rule: Fix diff bug by modifying 'DestCidrIp' to 'DestGroupId' when running read ([#35](https://github.com/terraform-providers/terraform-provider-alicloud/pull/35))


## 0.1.0 (June 20, 2017)

NOTES:

* Same functionality as that of Terraform 0.9.8. Repacked as part of [Provider Splitout](https://www.hashicorp.com/blog/upcoming-provider-changes-in-terraform-0-10/)
