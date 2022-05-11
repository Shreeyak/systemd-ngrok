## Installation - Manual

1. Install ngrok v3+ using apt/snap as on ngrok's [download page](https://ngrok.com/download).
2. Authenticate ngrok as per ngrok's [getting started page](https://dashboard.ngrok.com/get-started/your-authtoken). Add the `ssh` tunnel to ngrok's config file. Default location is: `~/.config/ngrok/ngrok.yml`.
3. (Alternate to step 2) Copy the `ngrok.yml` config file in this repo to `~/.config/ngrok/` and replace the authtoken in file with own.
4. Find the location of the `ngrok` executable using `whereis ngrok` and edit the `ExecStart` parameter in the `ngrok.service` file accordingly.
5. run the manual install script: `sudo manual_install.sh`. It copies the service file to the right location and enables the ngrok service using systemctl.

## Installation - Orig

1. Clone this repository to the target machine (eg: Raspberry Pi)
2. Get your `authtoken` from ngrok website
3. Inspect and modify the configuration file `ngrok.yml`, by default this config will use _Asia Pacific_ region to serve both **HTTP** and **TCP** tunnels
4. Run `sudo ./install.sh <your_authtoken>`, replace `<your_authtoken>` with the token you've obtained before from ngrok website.
5. You're good to go!

## Acknowledgements

Fork of: https://github.com/vincenthsu/systemd-ngrok
