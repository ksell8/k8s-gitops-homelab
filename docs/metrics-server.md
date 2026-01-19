# Why a Metrics Server?

We have a very limited number of resources.  We're running this on your computer.  We will need to know what is running hot on your computer.  This server makes and exposes it through `kubectl top`, which is also integrated with k9s.

If you install one of the other metrics services, there's not much need for this unless you need autoscaling services built off the metrics server.

[Metrics Server Code](https://github.com/kubernetes-sigs/metrics-server)
[Metrics Server Declaration](../infrastructure/base/metrics-server/)

