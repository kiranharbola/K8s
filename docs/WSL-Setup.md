Setup on Windows with WSL2:-

1) Install WSL https://docs.microsoft.com/en-us/windows/wsl/install
2) Install UBUNTU and latest Windows Terminal from marketplace
3) Insall kind on WSL https://kind.sigs.k8s.io/docs/user/quick-start/#installation [make a folder named "bin" on wsl root and added it to path]
   Steps:- echo $PATH (to see path) export PATH=$PATH:~/bin (to set bin to your PATH)
     To setup kind:-
     curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.11.1/kind-linux-amd64
     chmod +x ./kind
     mv ./kind /bin/kind
5) Install k9s https://k9scli.io/topics/install/ [curl -Lo k9s https://github.com/derailed/k9s/releases/download/v0.24.15/k9s_Linux_x86_64.tar.gz |  tar -xvf k9s]
6) Create cluster via kind [https://kind.sigs.k8s.io/docs/user/quick-start]
   Steps: create a yml file:-
   
    kind: Cluster
    apiVersion: kind.x-k8s.io/v1alpha4
    nodes:
    - role: control-plane
    - role: worker
    - role: worker
