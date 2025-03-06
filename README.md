# EXE Terminator Generator

## 📚 **Project Description**
The **EXE Terminator Generator** is a tool designed to automate the process of closing applications using the `taskkill` command in Windows. It addresses a recurring inefficiency in the Elementary Laboratory of Industrial Engineering at Gunadarma University, where assistants had to manually terminate applications on multiple computers. This tool simplifies the process by generating custom `.exe` files that can terminate specified applications with a single click.

---

## 🎯 **Goals**
1. **Automation**: Eliminate the need for manual intervention by automating the process of closing applications.
2. **User-Friendly Interface**: Create an intuitive GUI that allows users to easily generate custom `.exe` files.
3. **Scalability**: Ensure the tool can handle multiple target applications simultaneously.
4. **Ease of Deployment**: Generate `.exe` files that can be easily distributed and run on any Windows system.
5. **Customization**: Allow users to customize the generated `.exe` files with icons and other metadata using the Pillow library for image processing.

---

## 🛠️ **Tools and Technologies**
The project leverages the following tools and technologies:
- **Python**: The core programming language used for the application.
- **Tkinter**: Python's standard GUI library for creating the user-friendly interface.
- **Pillow**: A library for image processing, used to convert and embed custom icons into the generated `.exe` files.
- **PyInstaller**: A library for converting Python scripts into standalone `.exe` files.
- **Visual Studio Code**: The Integrated Development Environment (IDE) used for writing, debugging, and testing the code.
- **CMD (Command Prompt)**: Used for executing system commands like `tasklist` to search for running applications by their `.exe` name and `taskkill` to terminate specific processes programmatically.
- **DeepSeek AI**: An AI-powered coding assistant that helped optimize the code and implement features like the auto-slide banner and form validation.

---

## ⚙️ **Features**
The EXE Terminator Generator includes the following key features:
- **Custom EXE Generation**: Users can specify target applications and generate a custom `.exe` file to terminate them.
- **Icon Customization**: Using the Pillow library, the tool allows users to add custom icons to the generated `.exe` files.
- **Admin Privileges**: The generated `.exe` files can be configured to require admin privileges for execution.
- **Progress Indication**: A progress bar provides real-time feedback during the `.exe` generation process.
- **Error Handling**: The tool validates user inputs and provides informative error messages for issues like invalid file names or paths.

---

## 🧠 **Implementation**
The application is implemented using Python and several libraries to automate the process of generating custom `.exe` files for terminating applications. Below are the key components of the implementation:

### **Graphical User Interface (GUI)**
The GUI is built using **Tkinter**, providing an intuitive interface for users to input the target applications, specify the output `.exe` name, and customize the icon. The GUI also includes options to require admin privileges and open the output folder after generation.

### **Input Validation**
The tool validates user inputs to ensure:
- The target application names are valid.
- The output name does not contain invalid characters.
- The icon file is in a supported format (PNG, JPG, SVG, or ICO). If the icon is not in ICO format, the **Pillow** library is used to convert it.

### **PyInstaller Integration**
The core functionality of converting the Python script to a standalone `.exe` file is handled by **PyInstaller**. The tool constructs a command with parameters such as:
- `--onefile`: To create a single executable.
- `--noconsole`: To hide the console window.
- `--uac-admin`: To require admin privileges.

### **Threading for Responsiveness**
To ensure the GUI remains responsive during the `.exe` generation process, the tool uses **threading**. This allows the progress bar to update in real-time while the conversion runs in the background.

### **Error Handling**
The tool includes robust error handling to manage issues such as invalid inputs, PyInstaller errors, and file conversion failures. Informative error messages are displayed to guide users in resolving issues.

### **Cleanup**
After the `.exe` file is generated, the tool cleans up residual files such as the `.spec` file and the `build` directory created by PyInstaller. This ensures no unnecessary files are left behind.

---

---

## 🚀 **How to Use**
1. **Install Dependencies**:
   Ensure you have the required Python libraries installed:
   ```bash
   pip install pyinstaller pillow
2. **Run the Application**:
   Execute the Python script to launch the GUI:
   ```bash
   python exe_terminator_generator.py
3. **Generate a Taskkill EXE**:
   - Enter the target application names (comma-separated).
   - Specify the output executable name, icon (optional), and save location.
   - Choose advanced options like requiring admin privileges.
   - Click "Create Taskkill EXE" to start the process.
4. **View the Output**:
   Once the conversion is complete, the output `.exe` file will be saved in the specified       directory. If enabled, the output folder will automatically open.

---

## 📊 **Challenges and Solutions**
While developing this application, several challenges were encountered and resolved:
- Limited Coding Knowledge: Overcame by leveraging online resources, YouTube tutorials, and AI tools like DeepSeek.
- Handling Icon Conversion: Integrated the Pillow library to handle image conversion seamlessly.
- Ensuring Clean Output: Implemented a cleanup function to remove residual files generated by PyInstaller.
- User Experience: Added a user-friendly GUI using Tkinter to make the application accessible to non-technical users.

---

## 📝 **Recommendations for Improvement**
While the application is functional, there are areas where it can be improved:
- Error Handling: Provide more detailed error messages to help users troubleshoot issues.
- Batch Conversion: Add support for converting multiple Python files to executables in one go.
- Performance Optimization: Optimize the conversion process to reduce the time taken for large scripts.

---

## 🏁 **Conclusion**
The EXE Terminator Generator successfully automates the process of closing applications, significantly reducing the time and effort required for lab assistants. With its user-friendly GUI and advanced features, the tool demonstrates the potential of combining coding skills with practical problem-solving. The project also provided valuable learning opportunities in Python programming, GUI development, and debugging.

---

## 🛠️ **Dependencies**
To run this project locally, you need to install the following Python dependencies:
- PyInstaller: For converting Python scripts to executables.
  ```bash
  pip install pyinstaller
- Pillow: For image processing and icon conversion.
  ```bash
  pip install pillow
  
---

## 🤝 **Contributing**
Contributions are welcome! If you'd like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Submit a pull request.

---

## 🙏 **Acknowledgments**
While the application is functional, there are areas where it can be improved:
- DeepSeek AI: For providing valuable assistance in debugging and optimizing the code.
- Python Community: For the wealth of resources and libraries available.
- YouTube Tutorials: For helping me learn and implement various features.
