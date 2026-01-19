# What is kind?

BEING NICE TO PEOPLE.  It's the most important thing in the world.  But it's also a command line tool which stands for kubernetes in docker.  I used to use minikube.  But that's old school.  Minikube simulates a whole cluster in one container--boring.  Kind allows you to create multiple nodes as multiple docker containers.  A pretty simple differentiation, which is quite powerful under the hood.

### But Kurt, WTF is a cluster or a node.

OK, let's back up.  To run an application, we need compute (and probably storage, but let's start with the compute).  Compute means something that does computation.  A computer or a human, for eample (WARNING: a human will likely make a crappy cluster node).  For our current purposes, a cluster is a whole bunch of compute.  (It's really a container orchestrator, but hold your horses pedants, we're on a pedological path here.) 

This compute is split into two planes: a control plane and a data plane.  The control plane controls everything it takes to run the data plane, it's very boring work and 95% of companies pay a cloud provider (like Google or AWS) to manage it for them--because it's hard.  The data plane is the compute that runs your applications.

A [node](https://kubernetes.io/docs/concepts/architecture/nodes/) is a compute resource with a set number of resources that can be used to schedule work for the cluster.

# OK, enough, how do I set this up.

1) [Install kind](https://kind.sigs.k8s.io/docs/user/quick-start/#installation)
2) `kind create cluster`

### It can't be that easy?

Yeah, not really.  But this will create the default cluster to get you started with 1 node.

#### But Kurt, I wanna do fancy stuff with my kind.

[Okay nerd, RTFM](https://kind.sigs.k8s.io/docs/user/configuration/)