# Standalone ACI-Endpoint-Update-App

I. Installation Instructions

1. Prepare hosting VM, for example, Ubuntu 20.04 or 22.04.

2. Download install_aci_app_3.0.tgz

3. Untar install_aci_app_3.0.tgz:
   tar xzvf install_aci_app_3.0.tgz

You will find install_aci_app_3.0.sh under current directory.

4. Run install_aci_app_3.0.sh to start the app container, usage is as follows:

$ ./install_aci_app_3.0.sh

  Usage Example:

  ./install_aci_app_3.0.sh    # print this usage help

  ./install_aci_app_3.0.sh -s # Secure mode recommended for production. Configuration is accessible from localhost only, e.g. http://localhost:8000/configuration.json

  ./install_aci_app_3.0.sh -t # Test only, not recommended for production due to security reason. Configuration is accessible from any external host, e.g. http://<IP_of_this_host>:8000/configuration.json

  ./install_aci_app_3.0.sh -r # Run this to start an installed but exited ACI app container. Existing configuration would be kept.

For example, you may use "./install_aci_app_3.0.sh -s" to start the app in secure mode.

5. Launch a local browser to configure the app via the following URL:

http://localhost:8000/configuration.json



II. Security Notes

1. You should run the app in secure mode as you can to reduce security risk.

2. Use strong username/password to login to the hosting VM.

3. Hardening the hosting VM, including applying latest security patches, closing unused service ports etc.


