# Add_Skin Script  
**Add Skin to Namespace Merged Mod for Genshin Impact**  

## ✨ Overview  

The **Add_Skin** script is a powerful tool designed to help you seamlessly manage and merge skin mods for **Genshin Impact**. By dynamically handling `.ini` files and namespaces, it ensures easy integration of additional skins into a unified configuration, saving you time and reducing manual errors.

---

## 🚀 Features

### **Version 1.2 (Current)**

- **Merging Two Namespace Merged Mods**: V1.2 introduces the ability to merge two **namespace merged mods**. Enjoy greater flexibility by combining mods that were previously merged with other namespace mods.  
- **Folder Name Restrictions**: For error-free merging, ensure that all folder names (including subfolders) do not contain characters like `,` or `[]`.  
- **Increased Flexibility**: With V2, the script allows for more dynamic and robust handling of mods, offering better compatibility for namespace merged mods.  
- **Merging Requirements**: At least one namespace merged ini in required.

**Update**
- now the requirement for individual mods to be in subdirectory is no longer needed

### **Version 1 (Historic)**

- **Dynamic Namespace Handling**: Automatically updates namespaces in the `master.ini` file.  
- **Automated File Detection**: Scans the script directory and subfolders to find new `.ini` files.  
- **User Prompts**: Prompts the user to decide whether to include newly detected `.ini` files in the merged configuration.  
- **SwapVar Management**: Dynamically adds appropriate `swapvar` values for new skin mods.  
- **Compatibility**: Designed primarily for modding **Genshin Impact**, but adaptable for other use cases as well.

---

## 📋 Requirements  

- **Python 3.8.1** or later  
- Familiarity with `.ini` file configurations for **Genshin Impact** skin mods  
- A **namespace `.ini` file** (e.g., `master.ini`) in the same directory as the script.  
  [Genshin Impact Namespace Tool](https://gamebanana.com/tools/15681)

---

## 📝 Usage

1. Place the `Add_Skin` script in the folder containing your **namespace `.ini` file** (referred to as `master.ini`), as well as all the merged mod,s and individual mod,s to be merged.
2. **For merging two namespace merged mods**, Just place the another namespace merged mod in the same directory( or in subfolder) with script and the master ini(first namespace merged ini)
3. Make sure that **no folder names** (including subfolders) contain characters like `,` or `[]` to avoid issues.
4. Run the script by executing the following command:  
   ```bash
   python Add_SkinV1.2.py
5. Follow the on-screen prompts to decide whether to include or skip new .ini files.
6. The script will update the master.ini file with the correct namespaces and swapvar values.

## File Structure Example
```bash
├── Add_Skin1.2.py
├── master.ini
├── master2.ini(Another namespace merged ini)
├── master2/
│   ├── mod1(master2.ini merged folder 1)
│   ├── mod2(master2.ini merged folder 2)
├── skins mod3/
│   ├── mod3.ini
├── skins mod4/
│   ├── mod4.ini
├── skins mod5/(Mod folder for the mod to be added)
│   ├── mod5.ini(Mod ini to be added)
```
## 🛠️ How It Works

- The script identifies the namespace `.ini` file (usually `master.ini`) located in the same directory.
- It scans all subfolders for `.ini` files and dynamically matches paths and namespaces.
- It updates the `swapvar` numbers based on the highest existing value in the namespace `.ini` file.
- If you want to merge **two namespace merged mods**, the second **namespace merged `.ini` file** should be in the same directory as `master.ini`.
- Prompts the user for confirmation before integrating any new files into the merged configuration.

### Important Notes:
- The script can merge individual mods into the namespace `.ini` file.
- It can only merge another **namespace merged mod** if that mod was created using the **GIMI Mod Toggle Script**.  
  [GIMI Mod Toggle Script](https://gamebanana.com/tools/11165)  
  **In simple terms**: You can’t merge two namespace merged mods, but you can merge a **namespace merged mod** with a **GIMI merged mod**.

---

## 🤝 Contributing

We welcome contributions! If you encounter issues or have suggestions, feel free to open an issue or submit a pull request.

---

## 📝 License

This project is licensed under the **Creative Commons Attribution-NoDerivatives (CC BY-ND)** License. You are free to copy and share the project, but you are not allowed to modify or distribute any modified versions of it.

---

## ⚠️ Disclaimer

- This script is intended for personal, non-commercial use only.
- Always ensure you back up your files before using the script. Modding can lead to unexpected behavior in games, so proceed with caution.

---

## 🔮 Future Updates

- Support for custom namespace patterns    
- Enhanced compatibility with other games that utilize `.ini` mod systems  

## Future Updates

- Add support for custom namespace patterns.
- Implement logging for better error tracking and debugging.
- Enhance compatibility for other games with `.ini` mod systems.
