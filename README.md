# Diffuse Logic Framework - Packages

This folder contains zip files of the source code for the exact versions of the third-party repositories used by the framework.

**Purpose:**
1. **Fallback/Backup:** It acts as a reliable backup in case the original GitHub repository is temporarily unavailable, removed, or the network goes down.
2. **Build Accelerator:** It speeds up the initial CMake configuration significantly by allowing CPM to bypass the network download step entirely and use these local copies instead.

**Note:**
This folder (and its contents) is **totally optional**. If it doesn't exist or a zip is missing, the build system (CPM) will automatically fall back to downloading the requested version directly from GitHub.