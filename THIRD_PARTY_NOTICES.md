# Third-party notices

## Original work (this repository)

- **Copyright:** Lawrence Lo
- **License:** [MIT](LICENSE) at the repository root
- **Scope:** Original source and documentation in this tree (for example `Src/app/` beyond ST examples, `Src/framework/`, linker and README changes, and project-specific configuration such as `Inc/tx_user.h`). The MIT license does **not** relicense vendored components listed below.
- **ST Cube examples:** Files such as `Src/main.c` and `Src/app/ThreadX/app_tx_cmsisrtos.c` retain **STMicroelectronics** copyright and STM32Cube pack license terms unless replaced or substantially rewritten.

## Eclipse ThreadX

- **Version:** 6.5.2.202603_rel (see `Src/threadx/VERSION`)
- **Source:** [eclipse-threadx/threadx](https://github.com/eclipse-threadx/threadx) tag `v6.5.2.202603_rel`
- **License:** MIT (`Src/threadx/LICENSE.txt`)
- **In-tree subset:** `Src/threadx/common/`, `Src/threadx/ports/cortex_m33/gnu/` (no SMP, tests, or other ports)
- **Port init:** `Src/tx_initialize_low_level.S` (STM32U5 / CubeIDE; not the upstream `example_build` file)

## ST CMSIS-RTOS2 ThreadX wrapper

- **Location:** `Src/cmsis_rtos_threadx/`
- **License:** ST SLA0044 (see ST package / `README.md` in that folder)

## STM32 HAL / CMSIS

- **Location:** `Src/system/`
- **Licenses:** BSD-3-Clause (HAL), Apache-2.0 (CMSIS) per STM32Cube pack
