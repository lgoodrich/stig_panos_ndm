stig_panos_ndm
=========

A role to handle initial deployment or enforcement of NDM required STIG
configurations. Tested on virtual PANOS devices

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

```yaml
stig_ndm_pwcomplexity_enabled: 'yes'
stig_ndm_pwcomplexity_first_login_change: 'yes'
stig_ndm_pwcomplexity_min_length: 14
stig_ndm_pwcomplexity_min_history_count: 5
stig_ndm_pwcomplexity_min_ucase_letters: 1
stig_ndm_pwcomplexity_min_lcase_letters: 1
stig_ndm_pwcomplexity_min_numeric_letters: 1
stig_ndm_pwcomplexity_min_special_chars: 1
stig_ndm_pwcomplexity_min_char_diff: 8
stig_ndm_pwcomplexity_block_pwchange_period: 1
stig_ndm_pwcomplexity_max_exp_period: 60
stig_ndm_system_settings_tz: 'GMT'
stig_ndm_mgmtsettings_idle_timeout: 10
stig_ndm_mgmtsettings_log_high_dp_load: 'yes'
stig_ndm_cc_alarm_gen_enabled: 'yes'
stig_ndm_cc_alarm_gen_threshold_traffic: 75
stig_ndm_cc_alarm_gen_threshold_threat: 75
stig_ndm_cc_alarm_gen_threshold_config: 75
stig_ndm_cc_alarm_gen_threshold_system: 75
stig_ndm_cc_alarm_gen_threshold_alarm: 75
stig_ndm_cc_alarm_gen_threshold_hipmatch: 75
pan_mgmt_config_https_port: 443
pan_mgmt_config_primary_dns: '4.4.4.4'
pan_mgmt_config_secondary_dns: '8.8.8.8'
pan_mgmt_config_primary_ntp: '1.1.1.1'
pan_mgmt_config_secondary_ntp: '2.2.2.2'
pan_mgmt_config_primary_panorama: '1.1.1.3'
pan_mgmt_config_secondary_panorama: '1.1.1.4'
pan_mgmt_config_device_hostname: 'PA_VM'
pan_mgmt_config_login_banner: |
  You are accessing a U.S. Government (USG) Information System
  (IS) that is provided for USG-authorized use only. By using
  this IS (which includes any device attached to this IS), you
  consent to the following conditions:

  The USG routinely intercepts and monitors communications on
  this IS for purposes including, but not limited to,
  penetration testing, COMSEC monitoring, network operations and
  defense, personnel misconduct (PM), law enforcement (LE), and
  counterintelligence (CI) investigations.

  At any time, the USG may inspect and seize data stored on this
  IS.

  Communications using, or data stored on, this IS are not
  private, are subject to routine monitoring, interception, and
  search, and may be disclosed or used for any USG-authorized
  purpose.

  This IS includes security measures (e.g., authentication and
  access controls) to protect USG interests--not for your
  personal benefit or privacy.

  Notwithstanding the above, using this IS does not constitute
  consent to PM, LE or CI investigative searching or monitoring
  of the content of privileged communications, or work product,
  related to personal representation or services by attorneys,
  psychotherapists, or clergy, and their assistants. Such
  communications and work product are private and confidential.

  See User Agreement for details.
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

Lee Goodrich - ClearShark - Systems Engineer
