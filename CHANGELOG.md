# ghost-s3-storage-adapter

## 3.0.5
- fix issue with config (thx @norla)

## 3.0.3
- Name change to ghost-s3-storage-adapter

## 3.0.2
- Bug fix

## 3.0.1
- Bug fix

## 3.0.0
- Complete rewrite and implementation of delete and exists methods

## 2.0.1
- Forked [aorcsik/ghost-s3-storage-adapter](https://github.com/aorcsik/ghost-s3-storage-adapter) from [spanishdict/ghost-s3-compat](https://github.com/spanishdict/ghost-s3-compat)
- Initial changes to make it compatible with [ghost 0.10.0 breaking chnages](https://github.com/TryGhost/Ghost/wiki/Using-a-custom-storage-module#breaking-changes)

## 2.0.0

### Changed
- Restored the ability to specify an `assetHost` in the Ghost `config.js` file.
- Added logging on image serving errors.

### Fixed
- Use path-style URLs to construct the S3 endpoint images can be read from to
avoid certificate validation failures.  This is necessary because common bucket
naming can include one or more dots `(.)`, such as images.yourdomain.com. If you
a virtual-hosted–style URL https://images.yourdomain.com.s3.amazonaws.com would
fail a certificate validity check because AWS uses a \*.s3.amazonaws.com wildcard
cert. The certificate would be deemed invalid because RFC2818 allows matching of
only a single domain for a given wild card character.

## [1.0.2] - 2016-04-20
### Changed
- Add support for proxying local image requests to S3

## [1.0.1] - 2016-04-20
- Forked [spanishdict/ghost-s3-compat](https://github.com/spanishdict/ghost-s3-compat) from [muzik/ghost-s3](https://github.com/muzix/ghost-s3)
