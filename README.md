# ExplorerSvgSupport

## Description
**ExplorerSvgSupport** is a Windows File Explorer extension that provides thumbnail previews for SVG files. This allows users to see a preview of SVG images directly in File Explorer without opening an external viewer.

## How To Build
### Prerequisites
- Windows 10 or later
- Microsoft Visual Studio 2022 (Community Edition or higher)
- Qt 6.8.1 installed with MSVC 2022 support
- CMake (minimum version 3.14)
- Inno Setup 6 (for building the installer)

### Build Steps
1. **Clone the repository**:
   ```sh
   git clone https://github.com/rsmaxwell/ExplorerSvgSupport.git
   cd ExplorerSvgSupport
   ```

2. **Configure the project using CMake-gui**:
   - Open `CMake-gui`.
   - Set the **Source** directory to the root of the cloned repository.
   - Set the **Build** directory to a new `build` folder inside the repository (e.g., `ExplorerSvgSupport/build`).
   - Click **Configure** 
   - Click **Finish** to start the configuration process.
   - Click **Generate** to create the Visual Studio solution.
   - Once generation is complete, click **Open Project** to launch Visual Studio.

3. **Build the project in Visual Studio**:
   - Select `Release` configuration.
   - Build the solution (Ctrl + Shift + B).

4. **Build the installer**:
   Run the following script to generate the installer:
   ```sh
   BuildInstaller.bat
   ```

## How To Install
### Using the Installer
After building the installer, locate the generated `ExplorerSvgSupport-installer.exe` file in the `build/Release` directory.

1. **Run the installer**:
   ```sh
   ExplorerSvgSupport-installer.exe
   ```
2. Follow the on-screen instructions to complete the installation.
3. The extension should now be registered with Windows File Explorer.

### Verifying the Installation
- Open File Explorer and navigate to a folder containing `.svg` files.
- If the installation was successful, the thumbnails for `.svg` files should now be visible.

### Uninstallation
To remove **ExplorerSvgSupport**, you can:
- Use the **Windows Add/Remove Programs** feature.
- Or run the uninstaller from:
  ```sh
  C:\Program Files\ExplorerSvgSupport\unins000.exe
  ```

## Troubleshooting
If thumbnails do not appear after installation:
1. Restart File Explorer:
   - Open Task Manager (`Ctrl + Shift + Esc`)
   - Find **Windows Explorer**, right-click and select **Restart**
2. Restart your PC.
3. Ensure that **ExplorerSvgSupport.dll** is properly registered by running:
   ```sh
   regsvr32 C:\Program Files\ExplorerSvgSupport\ExplorerSvgSupport.dll
   ```

If you encounter any issues, feel free to [open an issue](https://github.com/rsmaxwell/ExplorerSvgSupport/issues).

---
**Author:** Richard Maxwell

Licensed under [MIT License](LICENSE.md).

