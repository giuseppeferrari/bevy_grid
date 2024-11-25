[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)]

A set of grids for storing and accessing data in a grid-like way.
Forked by sark_grid_rs by Sarkahn (https://github.com/sarkahn/sark_grids_rs)

This crate provides three types of grids:

- **[Grid](src/grid.rs)**: A dense grid that stores it's internal data in a `Vec`. The size of the grid is constant
and elements cannot be removed, only changed. Provides fast iteration and access speed.

- **[SparseGrid](src/sparse_grid.rs)**: A grid that stores it's internal data in a `BTreeMap`. Elements don't take up any memory until
they're inserted and can be removed as needed, but iteration and access speed will be slower than a `Grid` for large full grids.

- **[WorldGrid](src/world_grid.rs)**: A utility for translating between aligned grid points and world space.