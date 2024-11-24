**setup guideline** for installing and configuring Flutter using iTerm2 and FVM on macOS:

---

### **Step 1: Install iTerm2**
1. Download and install iTerm2 from [iterm2.com](https://iterm2.com/).
2. Open iTerm2 and proceed with the following steps.

---

### **Step 2: Install Homebrew**
- Install Homebrew for managing dependencies:
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```

---

### **Step 3: Install FVM (Flutter Version Manager)**
1. Install FVM using Homebrew:
   ```bash
   brew tap leoafarias/fvm
   brew install fvm
   ```

---

### **Step 4: Install Flutter via FVM**
1. Install the desired Flutter version:
   ```bash
   fvm install stable
   ```
   (Replace `stable` with a specific version if required, e.g., `fvm install 3.13.2`.)

2. Set the default Flutter version globally:
   ```bash
   fvm global stable
   ```

---

### **Step 5: Configure PATH for FVM**
1. Edit your shell configuration file:
   ```bash
   nano ~/.zshrc  # For zsh shell
   ```

2. Add FVM’s default binary path:
   ```bash
   export PATH="$PATH:$HOME/.fvm/default/bin"
   ```

3. Save the file and apply the changes:
   ```bash
   source ~/.zshrc
   ```

---

### **Step 6: Verify Installation**
- Verify Flutter installation through FVM:
  ```bash
  fvm flutter --version
  ```

---

### **Step 7: Set Up IDE**
1. Install your preferred IDE (e.g., **Visual Studio Code** or **Android Studio**).
2. Add Flutter and Dart plugins in the IDE.
3. Update the Flutter SDK path in the IDE to:
   ```plaintext
   ~/.fvm/versions/stable
   ```

---

### **Step 8: Create and Run a Flutter Project**
1. Create a Flutter project:
   ```bash
   fvm flutter create my_app
   ```

2. Navigate to the project directory:
   ```bash
   cd my_app
   ```

3. Run the project:
   ```bash
   fvm flutter run
   ```

---

This streamlined guideline sets up Flutter using iTerm2 and FVM on macOS efficiently.
