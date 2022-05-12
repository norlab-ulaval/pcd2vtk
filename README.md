# pcd2vtk
The following repository contains a command-line tool to convert PCD files to VTK format. This tool was developped by the PCL contributors/authors.

## Dependencies
This repository depends on PCL. To install PCL, run the following command in a terminal:
```bash
sudo apt install libpcl1-dev
```

## Compilation and installation
To install the pcd2vtk tool, run the following commands in a terminal at the root of this repository:
```bash
mkdir build && cd build
cmake ..
make
sudo make install
```

## Usage
```bash
pcd2vtk input.pcd output.vtk
```

