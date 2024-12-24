# Solution
* Setup kind-cluster
    ```bash
    $ kind create cluster --config kind-cluster.config.yaml
    ```
* Check nodes
    ```bash
    $ k get nodes -o wide
    ```
* Run container in "bash" mode
    ```bash
    $ docker exec -it <cluster> bash
    ```

* Update kubeadm (from 1.27 to 1.28)
    ```bash
    $ echo "deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.28/deb/ /" | tee /etc/apt/sources.list.d/kubernetes.list
    $ curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.28/deb/Release.key | gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
    $ apt update
    $ apt upgrade -y kubeadm
    ```

* Update cluster (from 1.27 to 1.28)
    ```bash
    $ kubeadm upgrade plan
    $ kubeadm upgrade apply v1.28.0
    ```

