# control-repo

Install r10k

```bash
puppet module install puppet/r10k --modulepath=/etc/puppetlabs/code/modules
puppet apply -e 'class{"r10k": remote => "https://github.com/the-paulus/control-repo" }' --moculdepath=/etc/puppetlabs/code/modules
r10k deploy environment -p
```
