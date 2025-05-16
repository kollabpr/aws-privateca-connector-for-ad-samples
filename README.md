# AWS Private CA Connector for Active Directory - Samples

This repository contains a PowerShell script (`adc-permissions.ps1`) that delegates the necessary permissions to your Active Directory trust store. **This script is mandatory only for customers who want to use AWS Private CA Connector for Active Directory (C4AD) with an [AD Connector](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_ad_connector.html) directory. 

## Purpose
- Automates the delegation of required permissions for AWS Private CA Connector for AD.
- Prevents permission-related errors during connector setup.

## Prerequisites
- Windows Server with Active Directory and the Active Directory PowerShell module installed.
- Sufficient privileges to modify permissions in your AD environment.

## Usage
Run the script in a PowerShell session with administrative privileges:

   ```powershell
   .\adc-permissions.ps1 -AccountName serviceAccountName
   ```
   
> **Note:** This script only works on root domains. If executed in a child domain, the script will display a warning and will not proceed. Ensure you are running the script in the root domain of your Active Directory forest.

## Feedback and Contributions
We welcome feedback and contributions from the community! Please open issues or submit pull requests to help improve the script. All contributions are subject to automated testing via GitHub Actions to ensure script quality and reliability.

## License
This project is licensed under the Apache License, Version 2.0. See the [LICENSE](LICENSE) file for details.

## Security
See [CONTRIBUTING.md](CONTRIBUTING.md) for security disclosure guidelines. 