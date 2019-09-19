# Batch Connect - OSC QGIS

![GitHub Release](https://img.shields.io/github/release/osc/bc_osc_qgis.svg)
[![GitHub License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

An interactive app designed for OSC OnDemand that launches QGIS within an Owens batch job.

## Prerequisites

This Batch Connect app requires the following software be installed on the
**compute nodes** that the batch job is intended to run on (**NOT** the
OnDemand node):

- [Lmod] 6.0.1+ or any other `module purge` and `module load <modules>` based
  CLI used to load appropriate environments within the batch job before
  launching the container.
- [rafdouglas/qgis_desktop] ([GPL licensed](https://github.com/rafdouglas/qgis_desktop_docker/blob/3.8/LICENSE)) which provides [QGIS] version 3.8.0 

[QGIS]: https://qgis.org/en/site/
[rafdouglas/qgis_desktop]: https://github.com/rafdouglas/qgis_desktop_docker
[Lmod]: https://www.tacc.utexas.edu/research-development/tacc-projects/lmod

## Install

Use Git to clone this app and checkout the desired branch/version you want to
use:

```sh
scl enable rh-git29 -- git clone <repo>
cd <dir>
scl enable rh-git29 -- git checkout <tag/branch>
```

You will not need to do anything beyond this as all necessary assets are
installed. You will also not need to restart this app as it isn't a Passenger
app.

To update the app you would:

```sh
cd <dir>
scl enable rh-git29 -- git fetch
scl enable rh-git29 -- git checkout <tag/branch>
```

Again, you do not need to restart the app as it isn't a Passenger app.

## Contributing

1. Fork it ( https://github.com/OSC/bc_osc_qgis/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
