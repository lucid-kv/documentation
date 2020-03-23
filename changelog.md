---
description: Lucid versions changelog.
---

# Changelog

## Lucid 0.1.4 Alpha

*  Improve CLI [\#47](https://github.com/lucid-kv/lucid/pull/47)
*  Finish Warp Migration [\#30](https://github.com/lucid-kv/lucid/issues/30)
  *  Graceful shutdown
*  Achieve PATCH Operations [\#44](https://github.com/lucid-kv/lucid/issues/44) [\#56](https://github.com/lucid-kv/lucid/pull/56)
  *  Lock / Unlock
  *  Increment / Decrement
  *  Define / Cancel Expiration
*  Persistence [\#17](https://github.com/lucid-kv/lucid/issues/17)
  *  Define file format and location
*  Encryption with Serpent [\#26](https://github.com/lucid-kv/lucid/issues/26)
  *  In-memory data encryption / decryption
*  Server Sent Event [\#27](https://github.com/lucid-kv/lucid/issues/27)
  *  Broadcast key update and creation
*  Improve Logging
  *  Add colored logs as an option
  *  Create output log file \(in /var/log/ under Unix\)
  *  Broadcast to `stderr` for warning or error entries

## Lucid 0.1.3 Pre-Alpha

* Mive Nickel-rs to Warp HTTP Core
* Improve CLI

## Lucid 0.1.0 - Pre-Alpha

### Added

* Lucid CLI Base \(with clap\)
* JWT generation
* Server base with API and WebUI endpoints
* Configuration files handling

