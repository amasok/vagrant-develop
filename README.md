前提条件

```
brew cask install vagrant cask  
brew cask install clipper ansible  
```

クローンする
```
git clone git@github.com:amasok/vagrant-develop.git  
cd vagrant-develop  
ansible-galaxy install -p ./provisioning/roles -r provisioning/requirements.yml  
vagrant up  
```

```
vagrant ssh-config --host [host_name] >> ~/.ssh/config  
```

vagrant内とlocalのcopyを同期する

```
# .ssh/configの[host_name]に以下を追記  
RemoteForward 8377 localhost:8377  
```
