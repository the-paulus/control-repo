# control-repo

Install r10k

```bash
puppet module install puppet/r10k --modulepath=/etc/puppetlabs/code/modules
puppet apply -e 'class{"r10k": remote => "https://github.com/the-paulus/control-repo" }' --moculdepath=/etc/puppetlabs/code/modules
r10k deploy environment -p
```

Encrypted YAML

```bash
puppetserver gem install hiera-eyaml
cd /etc/puppetlabs/puppet
eyaml createkeys
chown -R puppet:puppet ./keys
chmod -R 0500 ./keys
chmod 0400 keys/*.pem
```
