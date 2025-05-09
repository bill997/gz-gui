# Gazebo GUI : Graphical interfaces for robotics applications

**Maintainer:** jenn [AT] openrobotics [DOT] org

[![GitHub open issues](https://img.shields.io/github/issues-raw/gazebosim/gz-gui.svg)](https://github.com/gazebosim/gz-gui/issues)
[![GitHub open pull requests](https://img.shields.io/github/issues-pr-raw/gazebosim/gz-gui.svg)](https://github.com/gazebosim/gz-gui/pulls)
[![Discourse topics](https://img.shields.io/discourse/https/community.gazebosim.org/topics.svg)](https://community.gazebosim.org)
[![Hex.pm](https://img.shields.io/hexpm/l/plug.svg)](https://www.apache.org/licenses/LICENSE-2.0)

Build | Status
-- | --
Test coverage | [![codecov](https://codecov.io/gh/gazebosim/gz-gui/tree/gz-gui9/graph/badge.svg)](https://codecov.io/gh/gazebosim/gz-gui/tree/gz-gui9)
Ubuntu Noble| [![Build Status](https://build.osrfoundation.org/buildStatus/icon?job=gz_gui-ci-gz-gui9-noble-amd64)](https://build.osrfoundation.org/job/gz_gui-ci-gz-gui9-noble-amd64)
Homebrew      | [![Build Status](https://build.osrfoundation.org/buildStatus/icon?job=gz_gui-ci-gz-gui9-homebrew-amd64)](https://build.osrfoundation.org/job/gz_gui-ci-gz-gui9-homebrew-amd64)
Windows       | [![Build Status](https://build.osrfoundation.org/buildStatus/icon?job=gz_gui-9-clowin)](https://build.osrfoundation.org/job/gz_gui-9-clowin)

Gazebo GUI builds on top of [Qt](https://www.qt.io/) to provide widgets which are
useful when developing robotics applications, such as a 3D view, plots, dashboard, etc,
and can be used together in a convenient unified interface.

Gazebo GUI ships with several widgets ready to use and offers a plugin interface
which can be used to add custom widgets.

# Table of Contents

[Features](#features)

[Install](#install)

[Usage](#usage)

[Documentation](#documentation)

[Folder Structure](#folder-structure)

[Contributing](#contributing)

[Code of Conduct](#code-of-conduct)

[Versioning](#versioning)

[License](#license)

# Features

* Qt-based widgets, with support for both Qt5 widgets and QtQuick
* Plugin-based interface, so it's easy to add new widgets
* Several plugins ready to be used
* 3D scene integration using [Gazebo Rendering](https://github.com/gazebosim/gz-rendering/)

# Install

See the [installation tutorial](https://gazebosim.org/api/gui/9/install.html).

# Usage

Take a look at the
[tutorials](https://gazebosim.org/api/gui/9/tutorials.html)
for usage instructions and API documentation.

## Known issue of command line tools

In the event that the installation is a mix of Debian and from source, command
line tools from `gz-tools` may not work correctly.

A workaround for a single package is to define the environment variable
`GZ_CONFIG_PATH` to point to the location of the Gazebo library installation,
where the YAML file for the package is found, such as
```bash
export GZ_CONFIG_PATH=/usr/local/share/gz
```

Multiple paths can be specified using the `:` delimiter. For example,
```bash
export GZ_CONFIG_PATH=/user/local/share/gz/:/path/to/some/other/location
```

# Folder Structure

* `include/gz/gui`: Contains all the files which will be installed, such as
  C++ headers, `.qrc`, `.qss` and `qml` files. Plugin-specific resources go under
  `/plugins`; everything in the top-level is meant to be of common use across
  plugins.

* `src`: Contains all the C++ source code and headers which are not installed.
  Plugin-specific code goes under `/plugins`.

* `test`: All integration, performance and regression tests go here, under their
  specific folders.

* `examples/standalone`: Example code for standalone applications using Gazebo GUI
  as a library. Each example has instructions in a README file.

* `examples/config`: Example configuration files which can be loaded using
  `gz gui -c <path to file>`

* `examples/plugin`: Example plugins which can be compiled and loaded as explained
  in [this tutorial](https://gazebosim.org/api/gui/5.0/plugins.html).

* `tutorials`: Markdown files for the [tutorials](https://gazebosim.org/api/gui/5.0/tutorials.html).

* `conf`: Files needed by [gz-tools](https://github.com/gazebosim/gz-tools).

* `doc`: Files used by Doxygen when generating documentation.

# Contributing

Please see
[the contribution guide](https://gazebosim.org/docs/all/contributing).

# Code of Conduct

Please see
[CODE\_OF\_CONDUCT.md](https://github.com/gazebosim/gz-sim/blob/main/CODE_OF_CONDUCT.md).

# Versioning

This library uses [Semantic Versioning](https://semver.org/). Additionally, this library is part of the [Gazebo project](https://gazebosim.org) which periodically releases a versioned set of compatible and complimentary libraries. See the [Gazebo website](https://gazebosim.org) for version and release information.

# License

This library is licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0). See also the [LICENSE](https://github.com/gazebosim/gz-gui/blob/main/LICENSE) file.
