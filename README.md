# Add_Skin Script
Add Skin to namespace merged mod

## Overview

**Add_Skin** is a script designed for managing and merging skin mods for the game **Genshin Impact**. It dynamically handles `.ini` files and namespaces, allowing seamless integration of additional skins into a unified mod configuration. 

This script automates the process of identifying, merging, and updating skin mod configurations, saving time and reducing errors in manual editing.

---

## Features

- **Dynamic Namespace Handling**: Automatically updates namespaces in the `master.ini` file.
- **Automated File Detection**: Scans the script directory and subfolders for new `.ini` files.
- **User Prompts**: Asks the user whether to include newly detected `.ini` files in the merged configuration.
- **SwapVar Management**: Dynamically adds appropriate `swapvar` values for new skin mods.
- **Compatibility**: Designed specifically for modding **Genshin Impact**, but adaptable for similar use cases.

---

## Requirements

- **Python 3.8.1** or later
- A basic understanding of `.ini` file configurations for **Genshin Impact** skin mods.

---

## Usage

1. Place the `Add_Skin` script in the folder containing **only your namespace `.ini` file** (referred to as `master.ini`) and any subfolders with skin mod `.ini` files.
2. Run the script:
   ```bash
   python Add_Skin.py
3. Follow the on-screen prompts to include or skip new .ini files.
4. The script will update the master.ini file with the correct namespace and swapvar values.

## File Structure Example
├── Add_Skin.py
├── master.ini
├── skins/
│   ├── amber.ini
│   ├── nahida.ini
│   └── other_mods/
│       ├── mod1.ini
│       └── mod2.ini

## How It Works

- The script identifies the namespace `.ini` file (referred to as `master.ini`) in the same directory.
- Scans all subfolders for `.ini` files.
- Matches paths and namespaces dynamically.
- Updates `swapvar` numbers based on the last existing number in the namespace `.ini` file.
- Asks the user for confirmation before integrating new files.
- **Note:** The script can merge individual mods into the namespace `.ini` file. However, it can only merge another merged mod if that mod was merged using the **GIMI Mod Toggle Script**.  
  [GIMI Mod Toggle Script](https://gamebanana.com/tools/11165)

---

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

---

## License

This project is licensed under the **MIT License**.

---

## Disclaimer

- This script is intended for personal and non-commercial use.
- Ensure backups of your files before using the script, as modding can lead to unexpected behavior in games.

---

## Future Updates

- Add support for custom namespace patterns.
- Implement logging for better error tracking and debugging.
- Enhance compatibility for other games with `.ini` mod systems.
