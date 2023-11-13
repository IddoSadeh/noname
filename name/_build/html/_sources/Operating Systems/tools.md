*This page is a very rough first draft - work in progress*
# Installing and Updating Tools

Often we will need to update or install programs on our system or the system itself.

Updates should be done periodically, installing may be needed when you are missing a required program.

- We can upgrade and install all at once as follows, however it is not recommneded:

    `sudo su -` (change to the root user)

    `sudo apt update && apt upgrade` (get all the updates required, this will prompt you if you are sure you wish to continue. press no.)

    The reason this method is not recommneded is because sometimes updating everything at once may cause conflicts within our system.

    There are ways to update everything at once in a safe manner, for now stick to updating packages as needed.

- If you encounter a message of a missing package do the following:
    `sudo su -` (change to the root user)
    `sudo apt update`
    `sudo apt install package` (replace the word package with the name of the package you are missing)



<!-- Add section on Git -->