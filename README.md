## Creating a kubernetes cluster using kind
>Note that docker should be installed 

#### Install kind using curl command.
`curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.14.0/kind-linux-amd64`

#### Make the Kind binary executable.
`chmod +x kind`

#### Move the binary to a directory that is on your PATH.
`sudo mv kind /usr/local/bin/`

#### Verify that Kind is installed correctly by checking its version.
`kind version`

### create cluster using kind 
`kind create cluster --name=<cluster name>`

#### verify cluster is running
`kubeclt get node`
>if kubeclt command not found,
>install kubeclt using this command
`snap install kubeclt --classic`

#### Check the created cluster with get.
`kind get cluster`

### Pull a docker image.
`docker pull hello-world`

### Load the docker image.
` kind load docker-image hello-world`
