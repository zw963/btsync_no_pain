This small script is for quickly start synchronize data with ![BitTorrent Sync](https://getsync.com/) between your device.
should be start to work less than 10 seconds with internet connection(for download btsync binary only)

About BitTorrent Sync more Documents, Please refer to

* http://img.ezloo.com/docs/BitTorrentSyncUserGuide.pdf
* https://wiki.archlinux.org/index.php/BitTorrent_Sync
* http://help.getsync.com/hc/en-us/articles/204762669

## Philosophy
initialize a worked btsync config with minimum effort, make synchronize between two device
start to work imediately with NO PAIN.

It convenient for sync data between home/compary localnet pc, between host and virtual machine etc.
after change some config, can worked through internet. be careful to understood config completely
before do this.

## Requirement
need netcat installed (should be there in most UNIX like system)
Need BitTorrent Sync support this platform.

## Getting Started
Open your's terminal, input following:
```sh
  $ wget https://raw.githubusercontent.com/zw963/btsync_nopain/master/btsync_nopain
```
Run this script:
```sh
  $ bash btsync_nopain
```
Will ask you whether synchronized with READONLY access authority.

[![btsync_nopain1.png](https://zw963.github.io/btsync_nopain1.png)]

Press yes if you hope slave device can only sync but no change, or vice versa.

will See following WARN message for you:

[![btsync_nopain2.png](https://zw963.github.io/btsync_nopain2.png)]

Follow the instructions, goto slave device to complete configuration settings.

Basically, Open your's terminal in slave device, input following:

```sh
  $ nc MASTER_DEVICE_IP_address 2000
```

it Down! If lucky enough, btsync is syncing between master and slave device with folder ~/sync,
Just have a try.

## Support
should worked with any Unix system with netcat is installed.
currently not test with BSD like system, maybe exist bug.

## Limitations
* Windows is current not supported.
* BitTorrent Sync Web UI is closed.
* btsync is not open source, maybe use ![syncthing](https://github.com/syncthing/syncthing) instead.

## History
  See [CHANGELOG](https://github.com/zw963/btsync_nopain/blob/master/CHANGELOG) for details.
  
## Contributing
  * [Bug reports](https://github.com/zw963/btsync_nopain/issues)
  * [Source](https://github.com/zw963/btsync_nopain)
  * Patches:
    * Fork on Github.
    * Create your feature branch: \`git checkout -b my-new-feature\`.
    * Commit your changes: \`git commit -am 'Add some feature'\`.
    * Push to the branch: \`git push origin my-new-feature\`.
    * Send a pull request :D.
