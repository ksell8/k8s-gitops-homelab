# What is Flux?

[Flux](https://fluxcd.io/) is a declarative infrastructure as code framework.

Imperative programs manage state internally during execution. 
Any state that persists must be explicitly saved and loaded by your code.

Declarative programs rely on external state that persists between executions.
The system compares this state against your declarations and 
determines what actions to take.  In this case, our state is in k8s and driven by the desired state in this git repository.  Which is why flux is called Git Ops.  

# How do I install Flux in my Cluster?

1) [Install the Flux CLI](https://fluxcd.io/flux/installation/#install-the-flux-cli)
2) [Create a New Repository From this Template in Your GitHub](https://github.com/ksell8/k8s-monitoring-homelab)
3) [Create Yourself a Fine-Grained PAT for Your Repo](https://docs.github.com/es/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#fine-grained-personal-access-tokens)

    Needs: 
     - Administration -> Access: Read-only
     - Contents -> Access: Read and write
     - Metadata -> Access: Read-only

4) 

       flux bootstrap github \
           --token-auth \
           --owner=my-github-username \
           --repository=my-repository-name \
           --branch=main \
           --path=clusters/kind \
           --personal



[Official Docs](https://fluxcd.io/flux/installation/bootstrap/github/)

All the resources defined in [clusters/kind](https://github.com/ksell8/k8s-monitoring-homelab/tree/main/clusters/kind) will soon be in your cluster!