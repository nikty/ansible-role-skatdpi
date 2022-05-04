# Vasexperts SKAT DPI

# Role variables


`skatdpi_install_fastpcrf`: Install fastpcrf package

`skatdpi_install_fastdpi`: Install fastdpi  package

`skatdpi_configure_fastdpi`: Install fastdpi.conf

`skatdpi_configure_fastpcrf`: Install fastpcrf.conf

`skatdpi_enable_fastpcrf_service`: (bool) enable/disable fastpcrf service

`skatdpi_enable_fastdpi_service`: (bool) enable/disable fastdpi service

`skatdpi_delete_default_users`: (bool) Delete preconfigured users

`skatdpi_default_users_list`: (list) Preconfigured users list

`skatdpi_vasexperts_repo_rpm`: vasexperts repo package url

`skatdpi_vasexperts_repo_key`: vasexperts repo key url

`skatdpi_conf_dir`: Config directory

`skatdpi_udr`: Internal DB ("user data repository") (see `udr` in `fastdpi.conf`)

`skatdpi_ctrl_port`: `fastdpi.conf: ctrl_port` 

`skatdpi_ctrl_dev`: `fastdpi.conf: ctrl_dev`

`skatdpi_scale_factor`: `fastdpi.conf: scale_factor`

`skatdpi_num_threads`: `fastdpi.conf: num_threads` (https://wiki.vasexperts.ru/doku.php?id=en:dpi:dpi_components:platform:dpi_config:start#number_of_cores_threads)

`skatdpi_configure_censorship`: (bool) Whether to configure internet censorship (https://wiki.vasexperts.ru/doku.php?id=dpi:dpi_options:opt_filtration:filtration_settings:start)

`skatdpi_federal_black_list`: `fastdpi.conf: federal_black_list`

`skatdpi_black_list_redirect_url`: `fastdpi.conf: black_list_redirect`

`skatdpi_configure_netflow`: (bool) Whether to configure netflow

`skatdpi_netflow`: `fastdpi.conf: netflow`

`skatdpi_netflow_interface_name`: `fastdpi.conf: netflow_dev`

`skatdpi_netflow_full_collector`: `fastdpi.conf: netflow_full_collector`

`skatdpi_netflow_full_collector_type`: `fastdpi.conf: netflow_full_collector_type`

`skatdpi_netflow_rate_limit`: `netflow_rate_limit`

`skatdpi_configure_nat_logging`: (bool) Whether to configure NAT logging

`skatdpi_ipfix_dev`: `fastdpi.conf: ipfix_dev`

`skatdpi_ipfix_nat_udp_collectors`: (list) List of collectors, each one in the form as in `fastdpi.conf: ipfix_nat_udp_collectors`

`skatdpi_ipfix_nat_tcp_collectors`: (list) List of collectors, each one in the form as in `fastdpi.conf: ipfix_nat_tcp_collectors`

`skatdpi_configure_clickstream`: (bool) Whether to configure clickstream

`skatdpi_clickstream_ipfix_interface_name`: `fastdpi.conf: ipfix_dev`

`skatdpi_clickstream_ipfix_tcp_collectors`: (list) List of collectors, each one in the form as in **fastdpi.conf: ipfix_tcp_collectors**

`skatdpi_device_aliases`: dict of device aliases for use in `skatdpi_devices_in`, `skatdpi_devices_out`.
* key: device name
* value: "BUS:XXX" (https://wiki.vasexperts.ru/doku.php?id=dpi:dpi_components:platform:dpi_config:start#%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5_%D0%BF%D1%81%D0%B5%D0%B2%D0%B4%D0%BE%D0%BD%D0%B8%D0%BC%D0%BE%D0%B2_%D0%B4%D0%B5%D0%B2%D0%B0%D0%B9%D1%81%D0%BE%D0%B2)

`skatdpi_enable_auth`: `fastdpi.conf: enable_auth`

`skatdpi_fastpcrf_servers`: (list of dicts) List of dicts describing fastpcrf servers. This variable is used to construct `fastdpi.conf: auth_servers`
Dict keys:
* `ip`
* `dev`
* `port`

`skatdpi_enable_ipv6`: `fastdpi.conf: enable_ipv6`

`skatdpi_ctrl_trace`: `fastdpi.conf: ctrl_trace`

`skatdpi_fastpcrf_daemon`: `fastpcrf.conf: daemon`

`skatdpi_fastpcrf_verbose`: `fastpcrf.conf: verbose`

`skatdpi_fastdpi_servers`: List of dicts describing fastdpi servers. This variable is used to setup `fastpcrf.conf: fdpi_server` variables

`skatdpi_fastpcrf_coa_clients`: List of dicts describind coa_clients.
Dict keys:
* secret
* address
* dev
* port

https://wiki.vasexperts.ru/doku.php?id=en:dpi:dpi_options:opt_bras:bras_steps:radius_auth_fastpcrf_setup:start

Dict keys:
* `ip`
* `dev`
* `port`
* `params`: (dict)
    * param
    * value
  
`skatdpi_radius_servers`: List of dicts describing radius servers. This variable is used to setup `fastpcrf.conf: radius_server` variables
Dict keys:
* secret
* ip
* dev
* port

`skatdpi_radius_user_name_auth`: `fastpcrf.conf: radius_user_name_auth`

`skatdpi_fastpcrf_logs_trace`: `fastpcrf.conf: trace`

## Experimental

`skatdpi_configure_protocols_dscp`: (bool) Whether to configure `protocols.dscp`

`skatdpi_configure_binfiles`: (bool) Whether to configure various /etc/dpi/*.bin files
