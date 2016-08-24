# How to Use

This stack shows you how to setup a mono install with an external postgresql node that is installed with PE.

```
vagrant up;
vagrant ssh pe-mom -c "puppet enterprise configure; puppet agent -t"
vagrant ssh pe-postgres-node -c "puppet enterprise configure; puppet agent -t"
```

