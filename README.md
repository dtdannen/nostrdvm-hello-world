# nostrdvm-hello-world
Hello World DVM built using nostrdvm library

## Nostriga 2024 DVM Tutorial

1. Install python 3.12 
2. Create a virtual env
```commandline
python3.12 -m venv venv
```
3. Active the virtual env
```commandline
source venv/bin/activate
```

4. Install nostrdvm
```commandline
pip install nostr-dvm
```

5. Rename the DVM to something you'd like by changing the "DustinHelloWorldDVM" string
![name_of_free_dvm.png](docs%2Fname_of_free_dvm.png)

6. Run the DVM that does not require payment
```commandline
python main_no_payment.py
```

7. Navigate to https://dvmdash.live/playground
8. Submit a message and watch the DVMs respond

## To get started:
- Install Python 3.12


Create a new venv in this directory by opening the terminal here, or navigate to this directory and type: `"python -m venv venv"`
  - Place .env file (based on .env_example) in this folder.
  - Recommended but optional:
    - Create a `LNbits` account on an accessible instance of your choice, enter one account's id and admin key (this account will create other accounts for the dvms) Open the .env file and enter this info to `LNBITS_ADMIN_KEY`, `LNBITS_ADMIN_ID`, `LNBITS_HOST`.
    - If you are running an own instance of `Nostdress` enter `NOSTDRESS_DOMAIN` or use the default one.
  - Activate the venv with
    - MacOS/Linux: source ./venv/bin/activate
    - Windows: .\venv\Scripts\activate
  - Type: `pip install nostr-dvm`
  - Run `python3 main.py` (or python main.py)
  - The framework will then automatically create keys, nip89 tags and zapable NIP57 `lightning addresses` for your dvms in this file.
  - Check the .env file if these values look correct.
  - Check the `main.py` file. You can update the image/description/name of your DVM before announcing it.
  - You can then in main.py set `admin_config.REBROADCAST_NIP89` and 
    `admin_config.UPDATE_PROFILE` to `True` to announce the NIP89 info and update the npubs profile automatically.
  - After this was successful you can set these back to False until the next time you want to update the NIP89 or profile.

You are now running your own DVM. 
