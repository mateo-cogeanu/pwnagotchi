# How to Back Up Your Pwnagotchi

1. SSH into your Pwnagotchi.
2. Create a file called `backup.sh` using `nano`.
3. Add the contents of `backup.sh` (from this directory) into the file.
4. Save and exit.
5. Run the script with `sh backup.sh`.
6. Follow the process, and you will get a `.tgz` file.
7. Transfer the `.tgz` file to your local computer using `python -m http.server`.
8. In your web browser, go to `10.0.0.2:8000`, and you will see the `.tgz` file.
9. Click on the file to download it.

Now that you have the `.tgz` file, you can create a new Pwnagotchi, reset it, or make changes while keeping your data safe!

# How to Restore Your Pwnagotchi

1. SSH into the Pwnagotchi you want to restore.
2. Create a file called `restore.sh` using `nano`.
3. Copy the contents of `restore.sh` (from this directory) into the file.
4. Save and exit.
5. On your local machine, navigate to the directory containing your backup and run `python -m http.server`.
6. In your web browser, go to `10.0.0.1:8000` (your ip) and locate your `.tgz` file.
7. Copy the link to the `.tgz` file.
8. On the Pwnagotchi, run `wget http://10.0.0.1/YOUR.tgz` to download the file.
9. Run `sh restore.sh` and follow the instructions.
10. Restart your Pwnagotchi, and the restoration will be complete!
