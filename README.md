# Diffuse Logic Framework - Optional External Dependencies

This folder (`ext/optional/`) contains locally cached copies of third-party repositories and pre-compiled binary tools used by the framework.

## Structure

* **`packages/`**: Contains `.zip` files of the source code for third-party libraries.
  * **Fallback/Backup:** Acts as a reliable backup in case the original repository is temporarily unavailable or the network goes down.
  * **Build Accelerator:** Speeds up the initial CMake configuration significantly by allowing CPM to bypass the network download step and use these local copies instead.

* **`releases/`**: Contains pre-compiled binary releases (e.g., Slang compiler, GLEW binaries) as `.zip` files.
  * The `.zip` files are tracked by Git, but any extracted folders are automatically ignored.
  * Allows the build system to extract and use these pre-built tools without requiring manual internet downloads.

**Note:**
This entire folder (and its contents) is **totally optional**. If it doesn't exist or a zip is missing, the build system will automatically fall back to downloading the requested version directly from the web.