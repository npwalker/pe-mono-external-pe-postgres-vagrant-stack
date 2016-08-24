# How to Use

This stack shows you how to setup a mono install with an external postgresql node that is installed with PE.

The original installation of pe-mom will fail because the pe-postgres-node isn't created yet.

Once puppetserver is up and running though the pe-postgres-node can be installed.

Once the pe-postgres-node is installed then you can complete installation on pe-mom.

```
vagrant up pe-mom;
vagrant up pe-postgres-node;
vagrant ssh pe-mom -c "sudo su - -c 'puppet enterprise configure; puppet agent -t;'"
vagrant ssh pe-postgres-node -c "sudo su - -c 'puppet enterprise configure; puppet agent -t;'"
```

