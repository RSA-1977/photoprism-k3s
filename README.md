# photoprism-k3s

## Prerequisites

Before deploying `photoprism-k3s`, you need to have a Kubernetes cluster set up. Additionally, Longhorn, a distributed block storage system for Kubernetes, must be installed in your cluster.

To access PhotoPrism, ensure that `photoprism.test.com` resolves to the IP address of your Kubernetes nodes. This can typically be done by adding an entry to your local `/etc/hosts` file or configuring your DNS appropriately.

## To deploy the photoprism-k3s, follow these steps:

1. **Clone this repository:**

    ```sh
    git clone https://github.com/RSA-1977/photoprism-k3s.git
    ```

2. **Navigate to the photoprism-k3s directory:**

    ```sh
    cd photoprism-k3s
    ```

3. **Deploy the resources using kubectl:**

    ```sh
    kubectl create -k .
    ```

4. **Check the status of the pods in the photoprism namespace:**

    ```sh
    kubectl get pods -n photoprism
    ```

## Notes

- If Longhorn is not installed, follow the [Longhorn installation guide](https://longhorn.io/docs/1.6.2/deploy/install/install-with-helm/) to set it up.
- You can configure Photoprism to use NFS volumes instead of Longhorn. Look in ./statefulset/photoprism-statefulset.yaml for examples.
