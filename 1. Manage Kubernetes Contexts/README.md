### Questions:
1. **List All Kubernetes Contexts**  
   Write all Kubernetes context names into the file `/opt/course/1/contexts`.
   ```
   k config get-contexts
   ```

2. **Display Current Kubernetes Context with kubectl**  
   Write a command to display the current Kubernetes context create a file `/home/context.sh` and use this with `kubectl`.
   ```
   cd /home

   sudo touch context.sh

   sudo chmod +x context.sh

   echo "kubectl config current-context | sed s'/current-contexts: //'" | sudo tee /home/context.sh > /dev/null

   ./context.sh
   ```


3. **Display Current Kubernetes Context without kubectl**  
   Write a command to display the current Kubernetes context into the file `/home/context2.sh` without using `kubectl`.

   ```
   cd /home

   sudo touch context2.sh

   sudo chmod +x context2.sh

   echo "cat ~/.kube/config | grep current-context | sed s'/current-context: //'" | sudo tee /home/context2.sh > /dev/null

   ./context2.sh
   ```
