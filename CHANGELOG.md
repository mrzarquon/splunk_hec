# Change log

All notable changes to this project will be documented in this file. The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](http://semver.org).

## [v0.7.1](https://github.com/puppetlabs/puppetlabs-splunk_hec/tree/v0.7.1) (2019-07-01)

[Full Changelog](https://github.com/puppetlabs/puppetlabs-splunk_hec/compare/v0.7.0...v0.7.1)

### Fixed

- Fixes metrics uploading on splunk\_hec application [\#30](https://github.com/puppetlabs/puppetlabs-splunk_hec/pull/30) ([mrzarquon](https://github.com/mrzarquon))

## [v0.7.0](https://github.com/puppetlabs/puppetlabs-splunk_hec/tree/v0.7.0) (2019-06-25)

[Full Changelog](https://github.com/puppetlabs/puppetlabs-splunk_hec/compare/0.6.0...v0.7.0)

### Added

- Setup for github-changelog-generator [\#21](https://github.com/puppetlabs/puppetlabs-splunk_hec/pull/21) ([HelenCampbell](https://github.com/HelenCampbell))

### Fixed

- Adds troubleshooting documentation [\#22](https://github.com/puppetlabs/puppetlabs-splunk_hec/pull/22) ([mrzarquon](https://github.com/mrzarquon))

## 0.6.0
(2019/06/13)

### Changed
- The splunk_hec module now supports customizing the `fact_terminus` and `facts_cache_terminus` names in the custom routes.yaml it deploys. If you are using a different facts_terminus (ie, not PuppetDB), you will want to set that parameter. Please note that this will come with a breaking change in functionality - Switches to the fact terminus cache setting via routes.yaml to ensure compatibility with CD4PE, see Fact Terminus Support for guides on how to change it.

## 0.5.0
(2019/06/11)

### Added
- Advanced configuration for puppet:summary, puppet:facts and puppet:metrics to allow for the support of multiple indexes
- Additional documentation updates
- Added support for individual sourcetype urls
- Added ability to define multiple hec tokens on a sourcetype basis
- Addition of basic acceptance testing using Litmus
- The module is now under the power of the PDK
- Addition of the `saved_report` flag for the splunk_hec application - Allows the user to test some of the splunk_hec functionality, submits the result directly to the splunk configuration
- Addition of the splunk_hec puppet face/app allowing for a cat json | puppet splunk_hec like workflow. The primary functionality of this code is to enable sending pe metrics data to Splunk using the current CS best practices for collecting the CS data.
- Major changes to module were done to enable the Fact Terminus:
  - util/splunk_hec.rb created for common access methods
  - consistent info and error handling for both reports and facts
  - performance profile support for Fact Terminus
  - Documentation updated with guide and default facts listed
  - Module updated to optionally manage reports setting in puppet.conf
  - Module updated to add new parameters and template values
  - Fact collection time added to puppet report processor
  - SSL handling and documentation improved

### Fixed
- Minor fixes to output dialog

### Changed
- url parameter now expects a full URI of https://servername:8088/services/collector

## 0.4.1

- A small maintenance release to fix some broken links in metadata

## 0.4.0

Initial release

* SSL checking of target Splunk HEC is possible
* Submits Puppet Summary report
* Tasks for Bolt Apply and Bolt Result included
* Example Plans for above included


\* *This Changelog was automatically generated by [github_changelog_generator](https://github.com/skywinder/Github-Changelog-Generator)*
