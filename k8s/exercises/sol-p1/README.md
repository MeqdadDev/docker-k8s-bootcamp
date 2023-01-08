## Part 1:

1. You are required to deploy a nginx server version 1.23.3 through a yaml file

    Solution: [Here](nginx_dep_v1.23.3.yml)

2. Access the pod shell and update the default page to show your name.
    
    First of all, get the required nginx deployment name:
    ```bash
    kubectl get pod
    ```

    Use the name to access the pod's shell:
    ```bash
    kubectl exec -it nginx-deployment-db84444bd-c9qcl -- /bin/sh
    ```
    
    Add your name to the nginx default page:
    ```bash
    echo "Hi Meqdad from the default page in Nginx 1.23.3" > /usr/share/nginx/html/index.html
    ```
    
    Show the content of the nginx default page:
    ```bash
    cat /usr/share/nginx/html/index.html
    ```

3. restart the pod, and access the pod's page, what happened? can you explain?
    
    To restart the nginx deployment, there are many options, such as ```kubectl rollout restart``` command with this formula:
    ```bash
    kubectl rollout restart deployment <deployment_name> -n <namespace>
    ```

    In your case, you need to get the deployment name and namespace, which is ```default``` in our case, get your namespaces:
    ```bash
    kubectl get ns
    ```

    Now, apply the ```kubectl rollout restart``` command:
    ```bash
    kubectl rollout restart deployment nginx-deployment -n default
    --> deployment.apps/nginx-deployment restarted
    ```

    _Note_: After restarting, you'll notice that the name of your deployment is different, so get your new name before accessing the shell:
    ```bash
    kubectl get pod
    ```

    Re-access to the pod's shell using the new name:
    ```bash
    kubectl exec -it nginx-deployment-6569cd9b84-pdgs2 -- /bin/sh
    ```

    Finally, show the content of the nginx default page:
    ```bash
    cat /usr/share/nginx/html/index.html
    ```

    Result:
    You'll notice that the old content of nginx default page is printed! Which means that they deployment is a stateless process.