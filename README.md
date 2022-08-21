HOW TO RUN THE SCRIPT

1. Make sure ansible and python (apt install python3-pip python3.8-venv) already installed in the server (e.g 192.168.10.10)

2. Install Github Action on the server (e.g 192.168.10.10) and give unique name (e.g "simalpi")
   Edit .github/workflows/config-management.yml
   ```
   jobs:
     build:
       runs-on: simalpi
   ```

3. This script will run on server (e.g 192.168.10.10), as long as you set up the hosts to localhost
   If you expect to run on other hosts, you can write the IP on the "hosts" file
   ```
   [controller]
   localhost              ansible_connection=local
   
   [cloud]
   192.169.10.10
   ```

4. Go to roles/templates/requirements.txt, and try to edit version or add new module in requirements.txt file
   ```
   certifi==2022.6.15
   charset-normalizer==2.1.0
   idna==3.3
   ```

5. Set the project folder path in roles/vars/main.yml, change the "target" as you like
   ```
   target: /opt/xxx/xxx
   ```

6. Make a new commit and the script will run automatically.

==========================================================
python3 -m venv $name (create a venv)
source venv/bin/activate (activate venv)
pip3 list (listing all dependencies)
pip3 freeze > requirements.txt (export requirements file)
deactivate (deactivate venv)
===