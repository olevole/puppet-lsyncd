# puppet-lsyncd

# Usage
To configure a replication via a Puppet resource:
```puppet
lsyncd::rsync { 'myawesomereplication':
  source  => '/tmp/source',
  target  => '/tmp/target',
  options => {
    'archive': true,
  }
```

Or via Hiera:
```yaml
lsyncd::rsync:
  myawesomereplication:
    source: /tmp/source
    target: /tmp/target
    options:
      archive: true
```

# Notes

you may want to increase fs.inotify.max_user_watches sysctl params
