# mongodb-automation-agent
mongodb-automation-agent
NOTE: You will need an instance of MongoDB Ops Manager to be up and running before you can use an automation agent.
1. Clone this repo
2. Steps for bringing up an OpsManager can be found at : https://github.com/ksravikumar2005/mongodb-opsmanager-centos.git
3. Once the Ops Manager is up, gather the following details and populate them in the automation agent yml file
  URL:
  MMSID:
  GroupID:
 4. Bring up the automation agent and verify the agents on the OpsManager Console.
  docker stack deploy -c mongodb-automation-agent/docker-compose.yml <Stack name>
 
