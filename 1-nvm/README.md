## Step 1: Install nvm

### What is nvm?

nvm (Node Version Manager) is a tool that allows you to install and switch between different versions of Node.js and npm. This is useful because different projects may require different versions of Node.js. Ensuring all developers of a project use the same version reduces compatibility issues and "works on my machine" problems.

### Installation Instructions

We don't provide complete support nor instructions as here you will start a crucial part of your training, learning to scan for relevant information and applying that into your projects. Check out the following sections for further instructions:

#### For macOS/Linux:

1. **Open Terminal**:
   - You can open Terminal from the Applications folder or by searching for it using Spotlight.

2. **Download and Install nvm**:
   - Run the following command to download and install nvm:
     ```sh
     curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
     ```
   - This script clones the nvm repository to `~/.nvm` and adds the source lines to your profile (`~/.bash_profile`, `~/.zshrc`, `~/.profile`, or `~/.bashrc`).

3. **Load nvm**:
   - To start using nvm, you need to source your profile:
     ```sh
     source ~/.nvm/nvm.sh
     ```

4. **Verify Installation**:
   - To verify that nvm has been installed, run:
     ```sh
     command -v nvm
     ```
   - This should output `nvm` if the installation was successful.

#### For Windows:

1. **Download nvm for Windows**:
   - Go to the [nvm-windows repository](https://github.com/coreybutler/nvm-windows/releases) and download the latest `.exe` file.

2. **Install nvm for Windows**:
   - Run the installer and follow the setup instructions. The installer will add `nvm` to your PATH and create the necessary directories.

3. **Verify Installation**:
   - Open Command Prompt or PowerShell and run:
     ```sh
     nvm --version
     ```
   - This should output the version number of nvm if the installation was successful.

### Using nvm

1. **Install a Specific Version of Node.js**:
   - To install a specific version of Node.js, use the following command:
     ```sh
     nvm install <version>
     ```
   - For example, to install Node.js version 16.14.0, you would run:
     ```sh
     nvm install 16.14.0
     ```

2. **List Installed Versions**:
   - To see which versions of Node.js you have installed, use:
     ```sh
     nvm ls
     ```

3. **Switch Between Versions**:
   - To switch to a different version of Node.js, use:
     ```sh
     nvm use <version>
     ```
   - For example, to use Node.js version 16.14.0, you would run:
     ```sh
     nvm use 16.14.0
     ```

4. **Set a Default Version**:
   - To set a default version of Node.js to be used in any new shell, use:
     ```sh
     nvm alias default <version>
     ```
   - For example, to set Node.js version 16.14.0 as the default, you would run:
     ```sh
     nvm alias default 16.14.0
     ```

That's it! You have successfully installed nvm and are ready to install and manage multiple versions of Node.js.

### Next Steps

Once you have nvm and Node.js installed, you're ready to move on to the next steps in the setup process. Check out the following sections for further instructions:

- **Step 2: Install ESLint on VSCode**
- **Step 3: Install Prettier on VSCode**
- **Step 4: Learn about how derivables will be**

Happy coding!

---

*For more information about nvm, visit the [official nvm repository](https://github.com/nvm-sh/nvm).*


## Official Version to Use Throughout the Project

- Node.js: `22.3.0`. This is subject to change during the course.