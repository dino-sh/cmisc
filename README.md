# CMISC (Custom URI Scheme Creator)

CMISC is a Windows batch script tool designed to simplify the creation and management of custom URI schemes. These schemes enable applications to be launched using custom protocols, such as `myapp://action` or `myapp://subprotocol/action`. CMISC provides an easy-to-use interface for adding, managing, and deleting these schemes directly from the Windows registry.

## Features

- **Add Custom URI Schemes**: Register new URI schemes and associate them with applications.
- **Add Subprotocols**: Support nested subprotocols, like `myapp://sub1/sub2`.
- **Delete Existing URI Schemes**: Remove URI schemes and all associated subprotocols from the registry.
- **Safe Operations**: Automatically confirms user actions before modifying the registry.
- **User-Friendly Interface**: Interactive prompts guide users through the process.

## Requirements

- **Operating System**: Windows 7, 8, 10, or later.
- **Administrator Privileges**: The script requires admin access to modify the Windows registry.
- **Batch Script Support**: Built-in support for `.bat` files in Windows.

## Usage

### 1. Download CMISC

Clone the repository or download the `CMISC.bat` script file directly.

```bash
git clone https://github.com/dino-sh/cmisc.git
```

### 2. Run the Script

Right-click on the `CMISC.bat` file and select **Run as Administrator**.

### 3. Follow the Prompts

- **Add a URI Scheme**:
  - Enter the scheme name (e.g., `myapp`).
  - Provide the full path to the application (e.g., `C:\Path\To\App.exe`).
  - Optionally, specify subprotocols separated by slashes (e.g., `sub1/sub2`).

- **Delete a URI Scheme**:
  - Enter the scheme name to delete (e.g., `myapp`).

### 4. Verify Changes

To verify that the URI scheme has been registered or deleted:
1. Open the Registry Editor (`regedit`).
2. Navigate to `HKEY_CLASSES_ROOT`.
3. Look for the scheme name (e.g., `myapp`).

## Example

### Adding a URI Scheme

1. Run `CMISC.bat` as Administrator.
2. Select **[1] Add a new custom URI scheme**.
3. Provide details:
   - URI Scheme: `myapp`
   - Application Path: `C:\Apps\MyApp.exe`
   - Subprotocols: `action1/action2`
4. Confirm the input and the script will create the necessary registry entries.

### Deleting a URI Scheme

1. Run `CMISC.bat` as Administrator.
2. Select **[2] Delete an existing custom URI scheme**.
3. Enter the scheme name (e.g., `myapp`).
4. Confirm deletion and the script will remove the entries.

## Safety and Backup

- **Backup**: Before making changes, it's recommended to back up the registry. You can do this by exporting the `HKEY_CLASSES_ROOT` key in `regedit`.
- **Confirmation**: The script confirms all critical actions to prevent accidental modifications.

## License

This project is licensed under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests.

## Disclaimer

Use this script at your own risk. Modifying the Windows registry can have unintended consequences. Ensure you understand the changes being made before proceeding.

