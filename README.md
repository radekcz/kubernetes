# My kubernetes cheatsheet

--------------------------------

Autocomplete for kubernetes documentation for BASH:


source <(kubectl completion bash)  
echo "source <(kubectl completion bash)" >> ~/.bashrc  
alias k=kubectl  
complete -o default -F __start_kubectl k  
export do="--dry-run=client -o yaml"  
export now="--grace-period 0 --force"  
alias k='kubectl'  
alias kg='k get'  
alias kgp='k get pods'  
alias kd='k describe'  
alias kdp='kd pod'  
alias kns='k config set-context --current --namespace'  
alias kv='k config view --minify | grep namespace:'  

--------------------------------

Autocomplete for kubernetes documentation for ZShel:

source <(kubectl completion zsh)  
export do="--dry-run=client -o yaml"  
export now="--grace-period 0 --force"  
alias k='kubectl'  
alias kp='k get pods'  
alias kd='k describe'  
alias kdp='kd pod'  
alias kns='k config set-context --current'  
alias kv='k config view --minify | grep namespace:'  

--------------------------------

## Managing running pods

kubectl exec --stdin --tty <podname> -- /bin/sh

kubectl exec -it <podname> -- cat /log/my.log
