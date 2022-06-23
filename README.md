# ZPrize MSM on GPU Reference Test Harness

Example and reference testing harness for the ["Accelerating MSM on GPU"](https://assets.website-files.com/625a083eef681031e135cc99/629fd551a86dd7bd218dfd28_msm-gpu-fpga.pdf) challenge in ZPrize 2022.

## Build
The CUDA [`sppark`](https://github.com/supranational/sppark) from Supranational has a Rust binding. To install the latest version of Rust, first install rustup by following the instructions here, or via your platform's package manager. Once rustup is installed, install the Rust toolchain by invoking:

```
rustup install stable
```
After that, use cargo, the standard Rust build tool, to build the libraries:

```
git clone https://github.com/yelhousni/zprize-GPU-MSM-harness.git
cd zprize-GPU-MSM-harness
cargo build --release
```

## Test
To run a test of an MSM of `2^15` random points and scalars on the BLS12-377 curve, run:

```
cargo test --release
```

## Bench
This repository specifies default features corresponding to the zprize competition. To run the targer benchmark of the competition (`2^26` random points on BLS12-377), run:

```
cargo bench
```
