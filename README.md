# Permissions-configuration-by-Linux-commands

These are simple instructions about how to use Linux commands to alter files permissions.



## Step 1: Define current location and change it

First, we want to know in which directory we are right now. Then, we will move to another sub-directory we want to modify its permissions.

  ```bash
  pwd
  ```

  ```bash
  cd ./Labs
  ```

  ![Step 1](images/step1.png)
    
  ### Explanation
  - `pwd` is used to outline the current location.
  - `cd` -which stands for "change directory"- is used to change the current directory.
  - `./Labs` the directory we want to move to.

  > **Note:** A period `.` is put before the sub-directory to indicate that it is located in the current directory.


## Step 2: Check files or directories details

After moving to the required directory, we will use some commands to define the details about files and directories.

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
  -`ls` is used to outline contents of the current directory.
  -`ls -l` is used to outline the permissions of files and directories.
  -`ls -la` is used to outline the permissions of files and directories including hidden ones.
  - The permissions string consists of a 10-character string.
  - The first character demonstrates whether this is a file or directory.
  - The second, third and fourth characters indicates the user permissions of read `r`, write `w` and execute `x`.
  - The fifth, sixth and seventh characters indicates the group permissions of read `r`, write `w` and execute `x`.
  - The eighth, ninth and tenth characters indicates the other permissions of read `r`, write `w` and execute `x`.

  > **Note:** If one permission is revoked, it will be assigned as a hyphen `-`.


## Step 3: Modify permissions

If we want to change the permissions of any file, such as `photo.jpg`, to revoke write permissions of the group, we will use the `chmod` command -which stands for "change mode"-.

  ```bash
  chmod g-w photo.jpg
  ```

Now, to outline the changed we made, we use `ls -l` -we can use `ls -la` as well-.

  ```bash
  ls -l
  ```

  ![Step 3](images/step3.png)

  ### Explanation
  - `chmod` is used to modify permissions and it requires to arguments.
  - `g-w` indicates revoking group's write permissions.
  - `photo.jpg` the file we are modifying.

  > **Note:** `chmod` can contain letters and operators such as `+`, `-` or `=`. It can contain digits indicating permission values as well.
  > **Note:** We can modify more than one permission by separating them with comma `,`.



## Commands Used

  ```bash
  pwd
  cd ./relevant path
  ls
  ls -l
  ls -la
  chmod `user``operator``permission` file.txt
  ```



## What I Learned

  - How to communicate with the command-line.
  - File permissions in Linux and how to modify them.
  - How to define files details.



## License

This project is for educational purposes only.
