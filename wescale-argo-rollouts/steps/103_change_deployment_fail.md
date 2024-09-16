# The default way to deploy with Kubernetes : rolling-upgrade

We created for you a deployment in Kubernetes, named "webapp". look at the number of pods deployed with the command 

`kubectl get pods`{{execute}}

As you can see, all pods are healthy, which means the app should be working as expected.
.
You can access the page with the button "Open WebApp".

The current webapp is a simple webserver serving 3 files : `index.html`, `index.css` and `image.png`.

The deployment file is located in the file `manifests/deployment.yaml`

For the purpose of our demonstration, we will break the webserver by removing one of these files; The healthcheck will not 