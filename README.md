# photoprism-k3s

## Prerequisites

Before deploying `photoprism-k3s`, you will need to have a Kubernetes cluster deployed. Additionally, you need to have Longhorn installed in your Kubernetes cluster. Longhorn is a distributed block storage system for Kubernetes.

## To deploy the photoprism-k3s, follow these steps:

1. **Navigate to the photoprism-k3s directory:**

    ```sh
    cd photoprism-k3s
    ```

2. **Deploy the resources using kubectl:**

    ```sh
    kubectl create -k .
    ```

3. **Check the status of the pods in the photoprism namespace:**

    ```sh
    kubectl get pods -n photoprism
    ```

## Notes

- If Longhorn is not installed, follow the [Longhorn installation guide](https://longhorn.io/docs/1.6.2/deploy/install/) to set it up.
- You can configure PhotoPrism to use NFS volumes instead of Longhorn. Look in ./statefulset/photoprism-statefulset.yaml for examples.