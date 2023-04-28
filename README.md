# Autosar File Sorter

This program sorts an Autosar file based on the `<SHORT-NAME>` element using the lexicographical order. 

## Usage
1. Compile the program using `javac Main.java`
2. Run the program using `java Main Data.arxml`
3. A new sorted file will be generated with the name `Data_mod.arxml`

## Exceptions
The program can throw the following exceptions:
- `FileNotFoundException`: when no input file is provided
- `IllegalArgumentException`: when the input file does not have the `.arxml` extension
- `EmptyFileException`: when the input file is empty

## Code Explanation
- The program reads the input file and stores each line in an ArrayList of Strings
- It searches for the `<SHORT-NAME>` element in each line and stores the index of each occurrence in an ArrayList of Integers
- It compares the `<SHORT-NAME>` strings using the lexicographical order and swaps them if necessary
- After swapping, it moves the `<SHORT-NAME>` elements and the corresponding `<CONTAINER>` elements together
- The sorted lines are written to a new output file.
