### Auto-Scaling Master Instance

The [make_jenkins_EC2-autoscale.tmplt.json](/Templates/make_jenkins_EC2-autoscale.tmplt.json) template &mdash; along with deployment-automation helper-scripts &mdash; creates an EC2 Launch Configuration tied to an AutoScaling Group. This configuration is intended primarily to improve the availability of the Jenkins Master node. The AutoScaling group keeps the number of active nodes at "1": in the event of a failure detected in the currently-active node, the AutoScaling group will launch a replacement node. When the replacement node reaches an acceptable state, the original node is terminated.

The improved service-availability of this deployment mentod makes this is the preferred deployment template to use.
