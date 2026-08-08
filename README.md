# Linux File Permission Configuration

This project provides simple instructions for using Linux commands to modify file permissions.



## Step 1: Check the current location and change it

First, we want to know which directory we are currently in. Then, we will move to another sub-directory whose permissions we want to modify.

  ```bash
  pwd
  ```

  ```bash
  cd ./Labs
  ```

  ![Step 1](images/step1.png)
    
  ### Explanation
  - `pwd` is used to display the current working directory.
  - `cd` -which stands for "change directory"- is used to change the current directory.
  - `./Labs` specifies the `Labs` directory which is located in the current directory.

  > **Note:** `./` refers to the current directory.


## Step 2: Check file or directory details

After moving to the required directory, we will use several commands to inspect the files and directories.

  ```bash
  ls
  ```

  ```bash
  ls -l
  ```

  ```bash
  ls -la
  ```

  ![Step 2](images/step2.png)

  ### Explanation
  - `ls` is used to list the contents of the current directory.
  - `ls -l` is used to display the permissions of files and directories.
  - `ls -la` is used to display the permissions of files and directories including hidden ones.
  - The permissions field consists of a 10-character string.
  - The first character indicates the file type, such as a regular file `-` or a directory `d`.
  - The next nine characters represent the permissions for the user, group, and others.
  - The first three characters represent the user's permissions.
  - The next three characters represent the group's permissions.
  - The last three characters represent the permissions for others.
  - `r`, `w` and `x` represent "read", "write" and "execute" permissions.

  > **Note:** If a permission is not granted, it is represented by a hyphen `-`.


## Step 3: Modify permissions

If we want to change the permissions of any file, such as `photo.jpg`, to revoke write permissions from the group, we will use the `chmod` command -which stands for "change mode"-.

  ```bash
  chmod g-w photo.jpg
  ```

Now, to verify the changes we made, we use `ls -l` -we can use `ls -la` as well-.

  ```bash
  ls -l
  ```

  ![Step 3](images/step3.png)

  ### Explanation
  - `chmod` is used to modify file permissions and it requires a mode and one or more files.
  - `g-w` removes write permission from the group.
  - `photo.jpg` is the file whose permissions we are modifying.

  > **Note:** `chmod` supports symbolic modes using letters and operators such as `+`, `-` or `=`.
  > **Note:** `chmod` also supports numeric (octal) modes such as `755` and `644`.
  > **Note:** Multiple permissions can be modified by separating them with commas `,`.



## Commands Used

  ```bash
  pwd
  cd ./relevant_path
  ls
  ls -l
  ls -la
  chmod [who][operator][permission] file.txt
  ```



## What I Learned

- How to interact with the Linux command line.
- How Linux file permissions work and how to modify them.
- How to inspect file and directory details using Linux commands.



## License

This project is for educational purposes only.
