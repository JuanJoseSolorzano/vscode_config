# GitHub Copilot Instructions For Python Development

## General Guidelines
- Use concise and efficient code.
- Follow **PEP 8** for code style.
- Use **snake_case** for methods, variables, and function names.
- Use CamelCase for class names.
- Keep functions short and modular (max **60 lines**)

## Code Style & Best Practices
- Prefer list comprehensions over `map()` and `filter()`.
- Use **type hints** for better readability (`def foo(x: int) -> str:`)
- Follow **docstring** as follows:
    ```"""
    Description: __summary__.
    Parameters:
        - __name__ (__type__): __summary__.
    Returns:
        - (__type__): __summary__.
    """
    ```
    If `Parameters` or `Returns` are None, then avoid them.
- Prefer functions over inline logic.
- Write meaningful comments.

## Code Structure
- Keep functions **pure** (avoid modifying global state).
- Use `@staticmethod` and `@classmethod` when appropriate.
- Follow the **single-responsibility principle** (each function does one thing).
- Use context managers (`with open("file.txt") as file:`).

## Performance Optimization
- Use `set()` instead of [list](http://_vscodecontentref_/2) for membership tests (`if x in my_set:`).
- Avoid unnecessary loops (use `itertools` where possible).
- Use `dataclasses` for simple data structures instead of dictionaries.

## Avoid These Practices
- Avoid `from module import *` (use explicit imports).
- Avoid using `eval()` due to security risks.
- Avoid deep nesting in `if` statements (use early returns instead).
- Avoid global variables unless absolutely necessary.
- Avoid unnecessary variables (use `_` character when appropriate)

## Specific Rules
- Use list comprehensions in Python where possible.
- Check the grammar and coherence in the docstrings.
- Use the following file header for all .py files: 
    ```
    # -*- coding: UTF-8 -*-
    # ************************************************************************************************************#
    # COPYRIGHT (C) Vitesco Technologies                                                                          #
    # ALL RIGHTS RESERVED.                                                                                        #
    #                                                                                                             #
    # The reproduction, transmission or use of this document or its                                               #
    # contents is not permitted without express written authority.                                                #
    # Offenders will be liable for damages. All rights, including rights                                          #
    # created by patent grant or registration of a utility model or design,                                       #
    # are reserved.                                                                                               #
    # ------------------------------------------------------------------------------------------------------------#
    # Purpose:    Test Automation Framework                                                                       #
    # ************************************************************************************************************#
    # Tool chain: $Python:    >3.9                                                                                #
    # Filename:   $WorkFile:  <module_name>.py                                                                    #
    # Depencies:  $WorkFile:  <libraries/imports used>                                                            #
    # Revision:   $Revision:  1.0                                                                                 #
    # Author:     $Author:    <developer_name> (UID)                                                              #
    # Date:       $Date:      --/--/--                                                                            #
    # ************************************************************************************************************#
    # Module information:                                                                                         #
    # ------------------------------------------------------------------------------------------------------------#
    # Revisions:                                                                                                  #
    # [$Date] - <developer_name> (UID) - File creation.                                                           #
    # ************************************************************************************************************#
    ```
    Ensure the `Date` field in the file header is automatically updated to the current date.
