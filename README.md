# Solution for Ubuntu WSL Virtual Interface Issue

If you're facing an issue where only two virtual interfaces are available on Ubuntu running on Windows Subsystem for Linux (WSL), this solution will guide you to resolve it by switching back to WSL version 1.

## Steps to Resolve the Issue

### 1. Open Command Prompt or PowerShell as Administrator

First, open **Command Prompt** or **PowerShell** as an Administrator. You can do this by right-clicking on the Start menu and selecting "Command Prompt (Admin)" or "PowerShell (Admin)".

### 2. Set WSL Default Version to 1

Run the following command to set the default WSL version to **1**:

```bash
C:\Windows\System32>wsl --set-default-version 1

The operation completed successfully.
```

### 3. Check Installed WSL Versions

To check the installed WSL versions for your distributions, run this command:

```bash
C:\Windows\System32>wsl -l -v

NAME            STATE           VERSION
* Ubuntu-24.04    Stopped         2
```

### 4. Switch Ubuntu to WSL Version 1

Next, run the following command to convert your Ubuntu installation to **WSL version 1**:

```bash
C:\Windows\System32>wsl --set-version Ubuntu-24.04 1

Conversion in progress, this may take a few minutes.
The operation completed successfully.
```

### 5. Reopen Ubuntu

After the conversion is finished, reopen your Ubuntu instance. You should now see all your virtual interfaces restored.

## Conclusion

By following these steps, you can switch to WSL version 1 and restore the full set of virtual interfaces for your Ubuntu installation.

```

