# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

- Include hostname in redis cache keys  [#98](https://github.com/microsoft/planetary-computer-apis/pull/98)

## [2022.2.0]

### Changed

- Relative URLs on assets are rendered as absolute [#57](https://github.com/microsoft/planetary-computer-apis/pull/57)
- Update titiler-pgstac version to `0.1.0.a4` in `pctiler` [#46](https://github.com/microsoft/planetary-computer-apis/pull/46)
- Move render config, queryables and mosaic info into Azure Storage Tables [#48](https://github.com/microsoft/planetary-computer-apis/pull/48)
- Upgrades fastapi, stac-fastapi, and pgstac to 0.4.5 [#61](https://github.com/microsoft/planetary-computer-apis/pull/61)
- pcstac moves to Python 3.9, uvicorn, and min/max database connections limited to 1 [#73](https://github.com/microsoft/planetary-computer-apis/pull/73)
- Upgrades fastapi to 0.75.2 and fixes SwaggerUI vulnerability [#82](https://github.com/microsoft/planetary-computer-apis/pull/82)
- Render config generates correct querystrings when `render_options` contains list-like values [#85](https://github.com/microsoft/planetary-computer-apis/pull/85)
- Upgrade to pgstac 0.6.2 and corresponding stac-fastapi version. Supports more effecient hydration of STAC items and improved search performance. [#81](https://github.com/microsoft/planetary-computer-apis/pull/81)

### Added

- Added support for /queryables endpoint [#44](https://github.com/microsoft/planetary-computer-apis/pull/44)
- Added `/mosaic/info` endpoint [#48](https://github.com/microsoft/planetary-computer-apis/pull/48)
- Added caching and rate limiting to STAC API [#52](https://github.com/microsoft/planetary-computer-apis/pull/52)
- Added endpoint for interval legend classmap [#83](https://github.com/microsoft/planetary-computer-apis/pull/83)

### Fixed

- Fixed bug in legend/colormap endpoint [#53](https://github.com/microsoft/planetary-computer-apis/pull/53)
- Fixed tiler for Ground Control Point datasets, implemented for Sentinel 1 GRD [#90](https://github.com/microsoft/planetary-computer-apis/pull/90)


## [2022.1.3]

### Fixed

- Fixes and tests for item render links [#43](https://github.com/microsoft/planetary-computer-apis/pull/43)

## [2022.1.2]

### Fixed

- Fixed renderconfigs for item tile links [#41](https://github.com/microsoft/planetary-computer-apis/pull/41)
- Fixed hostname setting for URLs used in item links

## [2022.1.1]

### Fixed

- Fixed conformance classes [#39](https://github.com/microsoft/planetary-computer-apis/pull/39)
- Fixed STAC API version in API documentation [#39](https://github.com/microsoft/planetary-computer-apis/pull/39)

## [2022.1.0]

### Changed

- Upgraded stac-fastapi and pgstac versions to bring support for CQL2-JSON filter support [#20](https://github.com/microsoft/planetary-computer-apis/pull/20)
- Organized and updated documentation markdown docs [#11](https://github.com/microsoft/planetary-computer-apis/pull/11)
- Upgraded TiTiler to 0.4, includes changes to tile parameters [#22](https://github.com/microsoft/planetary-computer-apis/pull/22)
- Improved access logging [#23](https://github.com/microsoft/planetary-computer-apis/pull/23)
- Allow SAS URL variable to be passed to PC SDK in tiler service [#33](https://github.com/microsoft/planetary-computer-apis/pull/33)
- Upgrade to stac-fastapi 2.3.0 [#35](https://github.com/microsoft/planetary-computer-apis/pull/35)

### Added

- Errors are logged using exceptions and including request metadata [#14](https://github.com/microsoft/planetary-computer-apis/pull/14)
- Added endpoints to generate legends from colormap or registered classmaps [#17](https://github.com/microsoft/planetary-computer-apis/pull/17)
- Configuration for chloris-biomass, nrcan-landcover, noaa-c-cap
- Configuration for io-lulc-9-class [#34](https://github.com/microsoft/planetary-computer-apis/pull/34)
- Configuration for gnatsgo [#36](https://github.com/microsoft/planetary-computer-apis/pull/36)

### Fixed

- Updated search limit constraints to avoid 500s [#15](https://github.com/microsoft/planetary-computer-apis/pull/15)
- Fixed STAC `describedby` and `preview` links [#33](https://github.com/microsoft/planetary-computer-apis/pull/33)
- Default search limit restored to 250 [#36](https://github.com/microsoft/planetary-computer-apis/pull/36)
- Work around issue with LandPage stac_extensions [#37](https://github.com/microsoft/planetary-computer-apis/pull/37)
