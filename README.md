# cifar10 Federated Learning with nvflare
## OS Ubuntu 22.04
## follow the installer in base_install.txt, for the cuda installation there are several ways, remember to install the 11.8 version.

- project folder located in workspaces/secure_workspaces
- add in workspaces/secure_workspaces/admin@nvidia.com the "local" folder, required by nvflare.fuel.hci.tools.admin


## Relevant Features Change

- every client must have resources.json file in the local folder, this file can be inherited from resources.json.default ( remember to change the gpu mem from 0 )
- in startup/sub_start.sh file change the PYTHONPATH ( line 5) to :
export PYTHONPATH="${PYTHONPATH}:${PWD}/../local/custom"
required to find the learners etc..
- moved the pt/learner... folder in the local/custom folder of each client, server
- moved the prepare_data.sh in the transfer folder
- jobs folder moved to transfer folder in admin@nvidia.com 
