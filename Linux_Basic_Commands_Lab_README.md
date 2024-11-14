
# Linux Basic Commands Lab

## Scenario
You are working as a system administrator, and you need to organize files for a project. You will create directories, create files, move and copy files, and display their contents.

## Objectives
1. Create a directory structure for the project.
2. Create and manipulate files within these directories.
3. Use various commands to navigate and manage the files.

## Steps

### 1. Creating a Directory Structure
- Create a main project directory named `Project`.
- Inside `Project`, create two subdirectories: `Docs` and `Scripts`.

```bash
mkdir Project
cd Project
mkdir Docs Scripts
```

### 2. Creating Files
- Inside the `Docs` directory, create a file named `README.txt`.
- Inside the `Scripts` directory, create a file named `setup.sh`.

```bash
cd Docs
touch README.txt
cd ../Scripts
touch setup.sh
```

### 3. Using `echo` to Add Content to Files
- Add some text to `README.txt` and `setup.sh`.

```bash
echo "This is the README file for the Project." > ../Docs/README.txt
echo "#!/bin/bash" > setup.sh
echo "echo 'Setting up the project...'" >> setup.sh
```

### 4. Navigating the Directory Structure
- Go back to the main project directory and display the current directory.

```bash
cd ..
pwd
```

### 5. Listing Directory Contents
- List the contents of the `Project` directory.
- List the contents of the `Docs` and `Scripts` directories.

```bash
ls
ls Docs
ls Scripts
```

### 6. Displaying File Contents
- Display the contents of `README.txt` and `setup.sh`.

```bash
cat Docs/README.txt
cat Scripts/setup.sh
```

### 7. Copying and Moving Files
- Copy `README.txt` from `Docs` to the main `Project` directory.
- Move `setup.sh` from `Scripts` to the main `Project` directory.

```bash
cp Docs/README.txt .
mv Scripts/setup.sh .
```

### 8. Deleting Files and Directories
- Remove the `Docs` and `Scripts` directories.
- Remove the `README.txt` and `setup.sh` files from the main `Project` directory.

```bash
rm -r Docs
rm -r Scripts
rm README.txt
rm setup.sh
```

## Summary
In this lab, you:
- Created directories using `mkdir`.
- Created files using `touch`.
- Added content to files using `echo`.
- Changed directories using `cd`.
- Displayed the current directory using `pwd`.
- Listed directory contents using `ls`.
- Displayed file contents using `cat`.
- Copied files using `cp`.
- Moved files using `mv`.
- Deleted files and directories using `rm`.
