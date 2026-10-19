# Unreleased changes

Add here any changes made in a PR that are relevant to end users. Allowed
sections:

- Added - for new features.
- Changed - for changes in existing functionality.
- Deprecated - for soon-to-be removed features.
- Removed - for now removed features.
- Fixed - for any bug fixes.
- Security - in case of vulnerabilities.

Section headings should be at level 3 (e.g. `### Added`).

## Unreleased

### Added

- The TPU system metadata of runs on multi-host or multislice GKE TPU pods now includes the host's worker index and count within its slice and the slice index and count (`tpu.worker_id`, `tpu.worker_count`, `tpu.slice_id`, `tpu.num_slices`), read from the `TPU_WORKER_ID`, `TPU_WORKER_HOSTNAMES`, `MEGASCALE_SLICE_ID` and `MEGASCALE_NUM_SLICES` environment variables (@dmitryduev in https://github.com/wandb/wandb/pull/11792)
- Runs on Google Cloud now record the VM's project, zone and instance ID in their system metadata, plus the GKE cluster name and Kubernetes namespace when running in a GKE pod (@dmitryduev in https://github.com/wandb/wandb/pull/13206)

### Fixed

- `wandb leet symon` scaled the GPU PCIe and NVLink throughput charts and the Trainium memory charts by 1024³ on top of the bytes that the monitor reports, so their y-axis labels read like `7.67e+09GB/s` instead of `7.67GB/s` (@dmitryduev in https://github.com/wandb/wandb/pull/13191)
