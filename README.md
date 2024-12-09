---

# 📚 **Libft - Custom C Library with `ft_printf` and `get_next_line`**

![Libft](https://img.shields.io/badge/Libft-C_Library-blue?style=flat-square) ![C Programming](https://img.shields.io/badge/Language-C-brightgreen?style=flat-square) ![Makefile](https://img.shields.io/badge/Build-Makefile-yellow?style=flat-square)

Welcome to the enhanced **Libft** repository—a custom C library that includes reimplementations of essential C library functions, as well as `ft_printf`, `ft_printf_fd`, and `get_next_line`. This library is designed for modular use in future projects, offering flexibility and utility in formatted output, string manipulation, memory handling, and file reading.

---

## 📑 **Table of Contents**

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Technologies Used](#technologies-used)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Core Components](#core-components)
   - [Standard Library Functions](#standard-library-functions)
   - [Additional Utility Functions](#additional-utility-functions)
   - [`ft_printf` and `ft_printf_fd`](#ft_printf-and-ft_printf_fd)
   - [`get_next_line`](#get_next_line)
7. [Future Improvements](#future-improvements)
8. [Contributing](#contributing)
9. [Acknowledgements](#acknowledgements)
10. [Author](#author)

---

## 📖 **Introduction**

The enhanced **Libft** consolidates standard C library reimplementations, utility functions, `ft_printf`, `ft_printf_fd`, and `get_next_line`. This version adds flexibility with file descriptor-based formatted output while retaining consistency and modularity for use in various C projects.

---

## 📂 **Project Structure**

### Current Structure
```bash
.
├── include/           # Header files
│   └── libft.h        # Prototypes for all functions
├── src/               # Source files
│   ├── ft_*.c         # Core library functions
│   ├── ft_printf*.c   # Files for ft_printf and ft_printf_fd
│   ├── handle_*.c     # Modular handlers for specific printf cases
│   ├── get_next_line*.c # Files for get_next_line implementation
├── Makefile           # Makefile for building the library
├── README.md          # Project documentation
└── libft.a            # Compiled static library
```

### Suggested Modular Structure
If you plan to make the project more modular, consider the following structure:
```bash
.
├── include/           # Header files
├── src/
│   ├── core/          # Core libc reimplementations
│   ├── printf/        # ft_printf and its handlers
│   ├── gnl/           # get_next_line implementation
│   └── utils/         # Utility functions and helpers
├── Makefile
├── README.md
└── libft.a
```

---

## 🛠️ **Technologies Used**

- **C Programming**: Core language for implementing all functions.
- **Makefile**: Automates compilation.
- **GCC Compiler**: Compiles and links the source files into a static library.

---

## 🛠️ **Installation**

Follow these steps to build **Libft**:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/kitearuba/Libft-Enhanced.git
   ```

2. **Navigate to the Directory**:
   ```bash
   cd Libft-Enhanced
   ```

3. **Compile the Library**:
   ```bash
   make
   ```

The `libft.a` file will be created in the root directory.

---

## 🚀 **Usage**

Link the library in your projects for extended functionality.

1. **Include the Header in Your Code**:
   ```c
   #include "libft.h"
   ```

2. **Compile with the Library**:
   ```bash
   gcc -o myproject myproject.c -L. -lft
   ```

---

## 💻 **Core Components**

### 🔨 **Standard Library Functions**
Reimplementations of common libc functions for string manipulation, memory management, and type checking. Examples:
- `ft_isalpha`
- `ft_strlen`
- `ft_memset`
- `ft_strdup`
- And more.

### 🔧 **Additional Utility Functions**
Added functions like `ft_substr`, `ft_itoa`, and `ft_strjoin` provide more flexibility for handling strings and memory.

### 🌟 **`ft_printf` and `ft_printf_fd`**
#### **`ft_printf`**
A custom reimplementation of `printf` supporting:
- `%c`, `%s`, `%d`, `%i`, `%u`, `%x`, `%X`, `%p`, and `%%`.

#### **`ft_printf_fd`**
An extension of `ft_printf` that allows output to a specific file descriptor:
```c
ft_printf_fd(STDERR_FILENO, "Error: %s\n", "Something went wrong!");
```

### 📄 **`get_next_line`**
A function for reading a file line-by-line, supporting multiple file descriptors.

---

## 🌟 **New Features**
1. **`ft_printf_fd`**:
   - Dynamic output to any file descriptor.
   - Simplifies error handling by allowing direct output to `stderr`.

2. **Improved Code Modularity**:
   - Each aspect of `ft_printf` is split into manageable handler functions (e.g., `handle_char`, `handle_int`).

---

## 📈 **Future Improvements**
1. **Folder Restructuring**:
   - Modularize into `core`, `printf`, and `utils` directories for better organization.
2. **Dynamic Buffer Management**:
   - Extend `get_next_line` for variable buffer sizes.

---

## 🤝 **Contributing**

1. **Fork the Repository**.
2. **Create a Branch** (`git checkout -b feature/AmazingFeature`).
3. **Commit Changes** (`git commit -m 'Add some AmazingFeature'`).
4. **Push to Your Branch** (`git push origin feature/AmazingFeature`).
5. **Open a Pull Request**.

---

## 👨‍💻 **Author**

- **chrrodri**  
  [GitHub Profile](https://github.com/kitearuba)

---
