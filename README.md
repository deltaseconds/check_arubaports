
# check_arubaports

## Description

`check_arubaports` is a Perl script designed to monitor network interfaces on Aruba switches using SNMP (Simple Network Management Protocol). The script retrieves interface descriptions, operational statuses, and traffic statistics (incoming and outgoing bytes) from the switch and formats the data for easy readability.

## Usage

To run the script, you need to provide the hostname (IP address) of the Aruba switch. Optionally, you can specify the SNMP community string, SNMP version, and port number.

### Command Line Options

- `--hostname`: The IP address of the Aruba switch (required).
- `--community`: The SNMP community string (default: `public`).
- `--version`: The SNMP version to use (default: `2c`).
- `--port`: The port number for SNMP communication (default: `161`).
- `--help`: Display the usage information.

### Example
