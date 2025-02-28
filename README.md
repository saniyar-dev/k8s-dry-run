# k8s-dry-run
This repo is a workaround for actual and real dry-run in your k8s cluster. It's formed from a k8s custom scheduler which can be customized based on your needs to just export data from scheduling cycle and return these data in form of your needs.

## What i want to achieve?
As i searched for a actual dry-run on kubernetes clusters and there is no way to found out that the pod we want to schedule is going to really achieve state `Running` due to our limits and state of our k8s cluster or not, I thought it would be great if we have a tool which can provide us some data about scheduling pods on k8s cluster which really don't interrupt any process on the actual cluster but the behavior of this tool remain as same as the actual real status of our k8s cluster scheduler, so we can dry-run some scheduling process.

## There's a `dry-run` feature on kubectl, why you don't like it?
Due to [this documentation](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) using `kubectl dry-run` means that checking if we can send the `yaml` file to api-server or not.

**The table of options says this:**

 Name    | Defaul        | Usage  
 ------------- |-------------| ----- 
`dry-run`     | `none`        | Must be "none", "server", or "client". If client strategy, only print the object that would be sent, without sending it. If server strategy, submit server-side request without persisting the resource.

So, we can't achieve our goal by using this `dry-run` option. I think the name of this `kubectl` feature should be changed to something like verify!

## How can i know where's the progress of this project?
The progress will be tracked using [issue #1](https://github.com/saniyar-dev/k8s-dry-run/issues/1) so everyone can get onboard on progress and state of this project here.


## License
This repo uses GPL-v3.0 license which means any fork of this repo should be open-sourced too! For more information see `License` file.
