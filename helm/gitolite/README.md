# Usage

```
# installation
ssh-keygen -f $HOME/.ssh/id_rsa_test -N ""
helm upgrade --install   --set-file gitolite.SSH_KEY=$HOME/.ssh/id_rsa_test.pub  gitolite helm/gitolite

# make accessible
kubectl --namespace default port-forward service/gitolite 8080:22

# usage
ssh-add ~/.ssh/id_rsa_test
git clone ssh://git@localhost:8080/gitolite-admin
git clone ssh://git@localhost:8080/test


```
