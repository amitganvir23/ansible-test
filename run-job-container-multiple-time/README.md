### run galaxy to create role directory structure

- ansible-galaxy roles/server_info init
#### purpose
 - Run a job container and complete it
 - Inside of container there will be a jar file pasted
 - Jar will run some api call and connect with internel cluster running api server container

#### Playbook content some logic
  - Plybook run once because we have maintin skip task
  - Run a job container on kubernetes cluster using kubectl command
  - Created a template to run job container
  - Added single "when" and "block" condition for multiple api call
  - To run same playbook for multiple api, added "set_fact" and combined two variable togather and run loops in condition 

### test your playbook
- ansible-playbook deploy-test.yml
