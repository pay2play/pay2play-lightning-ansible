# Pay2Play Lightning Network Bitcoin Node Ansible DevOps Stack for Amazon AWS

## Dependencies
* sudo -H pip install pyyaml --upgrade
* sudo -H pip install boto3 --upgrade
* sudo -H pip install ansible

## Commands

### Lightning Node
* ansible-playbook -i inventory/hosts playbooks/start-node.yml
* ansible-playbook -i inventory/lightning playbooks/prepare-node.yml
* ansible-playbook -i inventory/lightning playbooks/deploy-bitcoin-daemon.yml

* ssh -i ~/.ssh/<YOUR_KEYPAIR_NAME>.pem ubuntu@ec2-<YOUR_EC2_IP>.<REGION>.compute.amazonaws.com

* ansible-playbook -i inventory/lightning playbooks/terminate-node.yml

## Misc
* ansible -i inventory all -m ping
* atom ~/.ssh/known_hosts
* docker logs bitcoind_mainnet --tail "10"

## Resources
* https://cloud-images.ubuntu.com/locator/ec2/
* https://bugs.launchpad.net/cloud-images/+bug/1458825/comments/2
* https://wiki.debian.org/Cloud/AmazonEC2Image

## Other
Questions? Ask us partner@pay2play.io
