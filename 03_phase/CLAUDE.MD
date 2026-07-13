# File Renaming Tool

## Project Objective

Create and maintain a safe utility that reads all `.txt` files from an `input` directory and creates renamed copies in an `output` directory using sequential filenames:

* `1.txt`
* `2.txt`
* `3.txt`
* and so on up to `n.txt`

The original files in the `input` directory must remain unchanged.

## Expected Directory Structure

```text
file-renaming-tool/
├── input/
│   ├── existing-file-a.txt
│   ├── another-file.txt
│   └── sample-document.txt
├── output/
├── CLAUDE.md
└── other project files
```

After execution:

```text
file-renaming-tool/
├── input/
│   ├── existing-file-a.txt
│   ├── another-file.txt
│   └── sample-document.txt
├── output/
│   ├── 1.txt
│   ├── 2.txt
│   └── 3.txt
├── CLAUDE.md
└── other project files
```

## Functional Requirements

1. Use a folder named `input` located in the project root directory.

2. Use a folder named `output` located in the project root directory.

3. Read only `.txt` files from the `input` directory.

4. Do not rename, move, delete, or modify the original files inside the `input` directory.

5. Create copies of the input files inside the `output` directory.

6. Rename the copied files sequentially as:

   ```text
   1.txt
   2.txt
   3.txt
   ...
   n.txt
   ```

7. Sort the input files alphabetically by their existing filenames before assigning the sequential numbers.

8. Process only files directly available inside the `input` directory.

9. Do not process files from subdirectories.

10. Create the `output` directory automatically if it does not already exist.

11. If the `input` directory does not exist, stop execution and display a clear error message.

12. If no `.txt` files are found in the `input` directory, display an appropriate message and do not create unnecessary files.

13. Preserve the complete content of every source file.

14. The content of each output file must be identical to the corresponding input file.

15. Existing files in the `output` directory must not cause incorrect numbering or filename collisions.

16. Before generating new output files, safely remove or replace only previously generated sequential `.txt` files such as:

```text
1.txt
2.txt
3.txt
```

17. Do not delete unrelated files from the `output` directory.

18. Display a clear mapping during execution, for example:

```text
another-file.txt -> 1.txt
existing-file-a.txt -> 2.txt
sample-document.txt -> 3.txt
```

19. Display the total number of files successfully created.

20. Do not make unrelated changes to the project without approval.

## Example

### Input Files

```text
input/
├── apple.txt
├── mango.txt
└── zebra.txt
```

### Generated Output Files

```text
output/
├── 1.txt
├── 2.txt
└── 3.txt
```

### File Mapping

```text
apple.txt -> 1.txt
mango.txt -> 2.txt
zebra.txt -> 3.txt
```

## Safety Rules

* Never modify files in the `input` directory.
* Never move files out of the `input` directory.
* Never delete source files.
* Never overwrite unrelated files in the `output` directory.
* Preserve the original file contents exactly.
* Process only `.txt` files.
* Do not process subdirectories unless explicitly approved.
