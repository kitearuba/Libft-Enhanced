
---

# 📚 **Libft - Custom C Library with ft_printf and get_next_line**

![Libft](https://img.shields.io/badge/Libft-C_Library-blue?style=flat-square) ![C Programming](https://img.shields.io/badge/Language-C-brightgreen?style=flat-square) ![Makefile](https://img.shields.io/badge/Build-Makefile-yellow?style=flat-square)

Welcome to the enhanced **Libft** repository, a custom C library that includes implementations of `ft_printf` and `get_next_line` along with essential C library functions. This version consolidates several useful functionalities into a single library, making it easy to reuse in future C projects.

---

## 📑 **Table of Contents**

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Technologies Used](#technologies-used)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Libft Functions](#libft-functions)
   - [Libc Functions](#libc-functions)
   - [Additional Utility Functions](#additional-utility-functions)
   - [ft_printf](#ft_printf)
   - [get_next_line](#get_next_line)
7. [Contributing](#contributing)
8. [Acknowledgements](#acknowledgements)
9. [Author](#author)

---

## 📖 **Introduction**

This enhanced version of **Libft** consolidates standard C library reimplementations, utility functions, the `ft_printf` function, and the `get_next_line` function into one cohesive library. It is designed to serve as a reusable toolkit for future C projects, offering functionality for string manipulation, memory handling, formatted output, file reading, and linked list management.

---

## 📂 **Project Structure**

```bash
.
├── include/           # Header files
│   └── libft.h        # Header file containing function prototypes
├── src/               # Source files implementing all required functions
│   ├── ft_*.c         # Source files for standard and custom functions
│   ├── ft_printf*.c   # Source files for ft_printf implementation
│   ├── get_next_line.c # get_next_line implementation
├── Makefile           # Makefile to compile the library
├── README.md          # This README file
└── libft.a            # Compiled library after running make
```

This structure ensures that the library is modular and easy to manage. Each C file focuses on a particular category of functions (e.g., string manipulation, memory management, formatted output, and file reading).

---

## 🛠️ **Technologies Used**

- **C Language**: The core language for implementing all functions.
- **Makefile**: Used to automate the compilation process.
- **GCC Compiler**: Compiles and links the C source files into the `libft.a` library.

---

## 🛠️ **Installation**

To get started with **Libft**, follow these steps to clone and build the library:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/kitearuba/libft.git
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd libft
   ```

3. **Compile the Library**:
   Simply run the `make` command to compile the library:
   ```bash
   make
   ```

After running `make`, you'll see the `libft.a` file, which is your compiled static library.

---

## 🚀 **Usage**

Once compiled, you can use **Libft** in your own C projects by linking it during compilation.

1. **Include the Header in Your Code**:
   ```c
   #include "libft.h"
   ```

2. **Compile Your Project with Libft**:
   You can link **Libft** with your project by specifying the path to `libft.a` during compilation:
   ```bash
   gcc -o myproject myproject.c -L. -lft
   ```

By using the `-L.` flag, you specify the current directory where the `libft.a` file is located, and the `-lft` flag tells the compiler to link against **Libft**.

---

## 💻 **Libft Functions**

This enhanced version of **Libft** includes the following components:

### 🔨 **Libc Functions**

You will find a set of functions from the C standard library (libc) prefixed with `ft_`. These functions handle common tasks like string and memory manipulation:

- `ft_isalpha`
- `ft_isdigit`
- `ft_isalnum`
- `ft_isascii`
- `ft_isprint`
- `ft_strlen`
- `ft_memset`
- `ft_bzero`
- `ft_memcpy`
- `ft_memmove`
- `ft_strlcpy`
- `ft_strlcat`
- `ft_toupper`
- `ft_tolower`
- `ft_strchr`
- `ft_strrchr`
- `ft_strncmp`
- `ft_memchr`
- `ft_memcmp`
- `ft_strnstr`
- `ft_atoi`
- `ft_calloc`
- `ft_strdup`

### 🔧 **Additional Utility Functions**

- `ft_substr`
- `ft_strjoin`
- `ft_strtrim`
- `ft_split`
- `ft_itoa`
- `ft_strmapi`
- `ft_striteri`
- `ft_putchar_fd`
- `ft_putstr_fd`
- `ft_putendl_fd`
- `ft_putnbr_fd`

### 🌟 **ft_printf**

**`ft_printf`** is a custom reimplementation of the C standard library's `printf` function. It supports the following conversions:
- `%c`: Prints a single character.
- `%s`: Prints a string.
- `%d`, `%i`: Prints an integer.
- `%u`: Prints an unsigned integer.
- `%x`, `%X`: Prints a hexadecimal number.
- `%p`: Prints a pointer address.
- `%%`: Prints a percent sign.

To use `ft_printf` in your project, include the `libft.h` header and link the `libft.a` library as shown in the [Usage](#usage) section.

### 📄 **get_next_line**

**`get_next_line`** is a function that reads a line from a file descriptor and returns it. It supports reading from any file descriptor (e.g., a file, standard input) and handles multiple file descriptors simultaneously.

Usage example:
```c
int fd = open("file.txt", O_RDONLY);
char *line = get_next_line(fd);
while (line)
{
    printf("%s", line);
    free(line);
    line = get_next_line(fd);
}
close(fd);
```

---

## 🤝 **Contributing**

Contributions are welcome! To contribute:

1. **Fork the Repository**.
2. **Create a Branch** for your feature or fix (`git checkout -b feature/AmazingFeature`).
3. **Commit Your Changes** (`git commit -m 'Add some AmazingFeature'`).
4. **Push to Your Branch** (`git push origin feature/AmazingFeature`).
5. **Open a Pull Request**.

Feel free to suggest improvements or request new features to enhance **Libft**!

---

## 🙌 **Acknowledgements**

A big thank you to the open-source community for their invaluable resources and contributions.

---

## 👨‍💻 **Author**

- **chrrodri**  
  [GitHub Profile](https://github.com/kitearuba)

---

## 🎉 **Final Thoughts**

Creating your own custom C library is a rewarding process that improves your understanding of low-level programming and memory management. **Libft** is just the beginning of your journey, and having this library will be a powerful tool in your future C projects.

Good luck, and happy coding! 🚀

---
