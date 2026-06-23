# USB Shortcut Virus Recovery Tool

A lightweight C# Windows Forms utility designed to clean USB drives infected by the notorious "Shortcut Virus." It safely deletes malicious `.lnk` files and restores hidden original folders and files to their normal state.

## Features
- **Malicious Shortcut Removal**: Scans and deletes fake `.lnk` files created by the virus.
- **File Attribute Restoration**: Reverses the hidden and system attributes applied to your original data, making them visible again.
- **Simple UI**: A clean Windows Forms interface for quick drive selection and execution.

## Development Environment & Requirements
- **OS**: Windows 11
- **IDE**: Visual Studio 2026
- **Framework**: .NET Framework 4.5.2

## How It Works
The tool automates the recovery process by programmatically identifying the target drive, removing shortcut files via `System.IO`, and safely executing the Windows attribute restoration command in the background:
```cmd
attrib -r -s -h /s /d [Target_Drive]:\*.*