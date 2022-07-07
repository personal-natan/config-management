HOW TO RUN THE SCRIPT

1. Make sure ansible and python already installed in the server (e.g 192.168.10.10)

2. Install Github Action on the server (e.g 192.168.10.10) and give unique name (e.g "simalpi")
   Edit .github/workflows/config-management.yml
   ```
   jobs:
     build:
       runs-on: simalpi
   ```

3. This script will run on server (e.g 192.168.10.10), as long as you set up the hosts to localhost
   If you expect to run on other hosts, you can write the IP on the "hosts" file.

4. Go to roles/templates/requirements.txt, and try to edit version or add new module in requirements.txt file

5. Set the project folder path in roles/vars/main.yml, change the "target" as you like.

6. Make a new commit and the script will run automatically.
