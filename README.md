# check_arubaports

## Overview
`check_arubaports` is a **Perl script** designed to monitor **network interfaces** on Aruba switches using **SNMP (Simple Network Management Protocol)**. It retrieves:

- **Interface descriptions**
- **Operational statuses** (UP/DOWN)
- **Traffic statistics** (incoming and outgoing bytes)

and formats the data for easy readability.

---

## Usage

To run the script, provide the **hostname** (IP address) of the Aruba switch. Optionally, specify the **SNMP community string**, **SNMP version**, and **port number**.

### Command Line Options

| Option         | Description                                      | Default |
|---------------|--------------------------------------------------|---------|
| `--hostname`  | The IP address of the Aruba switch (**Required**) | N/A     |
| `--community` | The SNMP community string                        | `public` |
| `--version`   | The SNMP version to use                          | `2c`     |
| `--port`      | The port number for SNMP communication           | `161`    |
| `--help`      | Display the usage information                    | N/A     |

### Example Command
```sh
perl check_arubaports.pl --hostname 192.168.1.1 --community private --version 2c --port 161
```

---

## Sample Output
```
1/1/1: DOWN | IN: 0.00 B, OUT: 0.00 B
1/1/10: DOWN | IN: 0.00 B, OUT: 0.00 B
1/1/37: UP   | IN: 898.50 KB, OUT: 2.43 MB
vlan1: UP    | IN: 0.00 B, OUT: 0.00 B
vlan150: UP  | IN: 0.00 B, OUT: 0.00 B
...
```

### Status Legend
- **UP** ✅ → Interface is active
- **DOWN** ❌ → Interface is inactive
- **IN/OUT Traffic** 📊 → Displays data transfer statistics

---

## Notes
- Ensure SNMP is **enabled** on your Aruba switch.
- The script **requires Perl** with SNMP support installed.
- Custom **thresholds** for monitoring can be implemented by modifying the script.

---

## License
This project is licensed under the **GNU General Public License v3.0**.

## Author
Developed by **deltaSeconds**.

