# platform-stm32u5-disco

Self-contained STM32CubeIDE project for **B-U585I-IOT02A**, based on ST `Tx_CMSIS_Wrapper` (ThreadX + CMSIS-RTOS2), with vendor HAL/CMSIS/ThreadX/BSP copied in-tree.

## Open in STM32CubeIDE

1. **File → Import → General → Existing Projects into Workspace**
2. Select root: `platform-stm32u5-disco-stm32ide` (folder containing `.project`)
3. Project name: **platform-stm32u5-disco**
4. **Project → Build Project** (Debug)

Debug launch: `platform-stm32u5-disco.launch` (expects `Debug/platform-stm32u5-disco.elf` after build).

## Layout (summary)

| Path | Role |
|------|------|
| `Inc/` | Application + `stm32u5xx_hal_conf.h`, `tx_user.h` |
| `Src/` | `main.c`, Cube MSP/IT, ThreadX low-level init |
| `Src/app/ThreadX/` | `app_tx_cmsisrtos.c` |
| `Src/system/include/` | CMSIS + STM32U5 HAL headers |
| `Src/system/src/cmsis/` | Startup, `system_stm32u5xx.c` |
| `Src/system/src/newlib/` | `syscalls.c`, `sysmem.c` |
| `Src/system/src/stm32u5xx/` | HAL sources (only demo subset built) |
| `Src/system/BSP/` | Board + components (vendored, not in build yet) |
| `Src/threadx/` | Eclipse ThreadX **6.5.2.202603_rel** (MIT; build: `common` + `ports/cortex_m33/gnu`) |
| `Src/cmsis_rtos_threadx/` | `cmsis_os2.c` |
| `Src/framework/` | Gallium framework (excluded from build until wired) |

## License

Original source and documentation in this repository (copyright Lawrence Lo) are under the [MIT License](LICENSE).

Bundled STM32 HAL/CMSIS, ST CMSIS-RTOS2 wrapper, Eclipse ThreadX, and BSP components keep their own licenses — see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
