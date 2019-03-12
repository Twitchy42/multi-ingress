# Multi-Ingress

Multi-Ingress is a chart built for deploying multiple nginx ingress controllers for kubernetes clusters on AWS. 

This chart assumes your cluster is using AWS as its cloud provider and that you are using Amazon Certificate Manager to secure your SSL endpoints

## Installing the Chart

To install the chart with the release name `my-ingress`

```console
$ helm install --name my-ingress multi-ingress --set identifier="foo" --set certificateARN="arn:aws:acm:...."
```

The command deploys multi-ingress on the Kubernetes cluster with an identifier tag and ACM certificate.

## Uninstalling the Chart

To uninstall/delete the `my-ingress` deployment:

```console
$ helm delete my-ingress
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

The following table lists the configurable parameters of the chart and their default values.

| Parameter                            | Description                                | Default                                                    |
| ------------------------------------ | ------------------------------------------ | ---------------------------------------------------------- |
| `identifier`                         | Unique identifying tag                     | `placeholder`                                              |
| `certificateARN`                     | AWS ACM ARN                                | `nil`                                                      |

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

## Reference Documentation:

[Multiple Ingress with ingress-nginx](https://kubernetes.github.io/ingress-nginx/user-guide/multiple-ingress/#multiple-ingress-nginx-controllers)

[Deploying ingress-nginx on AWS](https://kubernetes.github.io/ingress-nginx/deploy/#aws)