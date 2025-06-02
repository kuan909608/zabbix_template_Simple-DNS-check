# Zabbix Template - Simple DNS Check

This project provides a Zabbix YAML template for checking DNS availability and response time using external checks. It is designed for lightweight DNS health monitoring scenarios.

## Features

- Check if DNS queries are successful (non-empty result)
- Measure DNS response time
- Trigger alerts on DNS lookup failures or timeouts
- Compatible with Zabbix 6.0 LTS and later

## Import Instructions

1. Log in to Zabbix Web Console.
2. Go to `Configuration` > `Templates`.
3. Click `Import` at the top-right corner.
4. Select the `zabbix_template_simple-dns-check.yaml` file.
5. Review and confirm the import options.

## How to Use

1. Link the template to your host(s).
2. Ensure that the host has `dig` or `nslookup` installed.
3. Modify the item parameters to fit your domain/query needs.
4. Customize triggers or graphs as needed.

## Notes

- Make sure the Zabbix Server or Proxy has access to the `ExternalScripts` directory.
- DNS tools (e.g., `dig`) must be installed on the execution host.
- If using internal DNS servers, adjust the target IP accordingly.

## License

This project is released under the MIT License. Feel free to use and modify.
