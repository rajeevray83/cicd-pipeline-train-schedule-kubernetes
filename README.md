# cicd-pipeline-train-schedule-kubernetes

** Ian's copy **
This is a simple train schedule app written using nodejs. It is intended to be used as a sample application for a series of hands-on learning activities.

## Running the app alone

You need a Java JDK 7 or later to run the build. You can run the build like this:

    ./gradlew build

You can run the app with:

    ./gradlew npm_start

Once it is running, you can access it in a browser at http://localhost:8080

## Running on Kubernetes
It runs on a nodePort on 8080 which is not available by default. Thus it requires modification
of the manifest (config file) /etc/kubernetes/manifests/kube-apiserver.yaml to contain the line '- --service-node-port-range=8080-32767'

#added githook
