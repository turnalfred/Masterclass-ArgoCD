Argo installations come in two flavours
- Core 
    - 
- Multi-Tenant
    - typically used to service multiple application developer teams in the organization and maintained by a platform team.


Steps for Installation
1. Create `argocd` namespace 
    ```bash
    kubectl create namepace argocd
    ``` 
2. Download Manifest Files [Install manifests](https://raw.githubusercontent.com/argoproj/argo-cd/master/manifests/install.yaml)
    #### *nix*
    ```bash
    curl -L https://raw.githubusercontent.com/argoproj/argo-cd/master/manifests/install.yaml > argo-install.yaml
    ```
    #### Windows
    ```powershell
    Invoke-WebRequest -Uri "https://raw.githubusercontent.com/argoproj/argo-cd/master/manifests/install.yaml" -OutFile "argo-install.yaml"
    ```
3. Apply the downloaded manifests to your Kubernetes Cluster
    #### *nix /Windows
    ```bash
    kubectl apply -n argocd -f argo-install.yaml
    ```
## Configure  and port Forward API Server for cli Access
> [!CAUTION]
>
> THESE SETUOS SHOULD NEVER BE PERFORMED IN PRODUCTION
> CREATE AND USE A VALID SSL CERT IN PRODUCTION 
> THIS IS FOR DEMO PURPOSES ONLY

4. 

