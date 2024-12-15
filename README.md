### **Node.js Minecraft Bedrock Add-on Compiler and Development Environment**

A lightweight and efficient toolset for Minecraft Bedrock add-on developers, built with Node.js. This library simplifies the creation, synchronization, and deployment of Behavior Packs (BP) and Resource Packs (RP), providing a seamless development experience with features like real-time file watching, automated directory management, and JSON handling.

---

## **Features**
- 🔄 **Automatic File Synchronization**: Sync your `BP` and `RP` directories directly to the `com.mojang` development folder.
- 📂 **Recursive Directory Management**: Handles nested folders and files for complex projects.
- 👀 **File Watcher**: Real-time monitoring and syncing of changes for faster iterations.
- 📝 **JSON Handling**: Minifies and processes JSON files for optimized performance.
- 🌟 **Customizable Destination**: Switch between stable and beta versions of Minecraft with ease.

---

## **Installation**

```bash
npm install minecraft-addon-compiler
```

---

## **Usage**

### **CLI Commands**
Run the tool using Node.js and customize it through CLI arguments:

```bash
node index.js [options]
```

### **Options**
| Option          | Description                                              | Default       |
|------------------|----------------------------------------------------------|---------------|
| `--init`         | Run a full sync on startup.                              | `true`        |
| `--dest stable`  | Set the destination to the stable version of Minecraft.  | `stable`      |
| `--dest beta`    | Set the destination to the beta version of Minecraft.    | `stable`      |
| `--watch`        | Enable real-time file watching and syncing.              | `false`       |

### **Examples** 
1. **Full Sync (Stable)**
   ```bash
   node index.js --init true --dest stable
   ```

2. **Sync and Watch (Beta)**
   ```bash
   node index.js --watch --dest beta
   ```

---

## **Folder Structure**  

Ensure your project structure follows this format for proper syncing:

```plaintext
Project Folder
├── BP/                  # Behavior Pack files
│   ├── manifest.json
│   ├── entities/
│   └── ...
├── RP/                  # Resource Pack files
│   ├── manifest.json
│   ├── textures/
│   └── ...
└── index.js             # Script entry point
```

---

## **How It Works**

1. **Source Folders**: Syncs the `BP` and `RP` directories in your project folder.
2. **Destination Folders**: Automatically detects the `com.mojang` path based on the Minecraft version (stable or beta).
3. **File Handling**:
   - Minifies JSON files.
   - Handles nested directories and ensures all files are copied.
   - Watches for changes and updates files in real-time.

---

## **Contributing**

Feel free to contribute to this project by submitting issues or pull requests. Feedback and feature suggestions are welcome!

---

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.
