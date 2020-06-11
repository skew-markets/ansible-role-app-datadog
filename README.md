----
# ansible-role-app-datadog

## Purpose
Installs and enables a DataDog agent

## Required variables
| Name | Description |
| ---- | ----------- |
| datadog_api_key | the value DataDog provide you when you signed up |

## Defaulted variables
| Name | Value | Description |
| ---- | ----- | ----------- |
| datadog_agent_enabled | true | systemd flag |
| datadog_agent_status | started | systemd flag |
| datadog_arch | x86_64 | i386 is not supported |
| datadog_cfg_file | '{{datadog_etc_dir}}/datadog.yaml' | would only change if Datadog changed things |
| datadog_etc_dir | /etc/datadog-agent | would only change if Datadog changed things |
| datadog_group | dd-agent | would only change if Datadog changed things |
| datadog_handler | handler_restart_datadog | |
| datadog_owner | dd-agent | would only change if Datadog changed things |
| datadog_pubkey_id | 382E94DE | Used for APT repo |
| datadog_repo_url | datadoghq.com | Used for YUM repo |
| datadog_state | present | set to absent to uninstall |
| datadog_svc_name | datadog-agent | would only change if Datadog changed things |

## Optional variables
| Name | Value | Description |
| ---- | ----- | ----------- |
| datadog_tags | dict | Used to tag hosts in the Datadog console |

Also, if you add a dictionary called 'datadog' to host or group vars, its contents will be set as tags in Datadog

## Supported Distros
- Ubuntu 16
- Ubuntu 18
- Amazon Linux 2

## Untested, but should work
- CentOS 7+
- RHEL 7+ if using systemd
- Ubuntu 20

****
