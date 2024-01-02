# STM32CubeL0 MCU Firmware Package

![latest tag](https://img.shields.io/github/v/tag/STMicroelectronics/STM32CubeL0.svg?color=brightgreen)

## Important note

This repository has been created using the `git submodule` command. Please refer to the ["How to use"](README.md#how-to-use) section for more details.

## Overview

**STM32Cube** is an STMicroelectronics original initiative to ease developers' life by reducing efforts, time and cost.

**STM32Cube** covers the overall STM32 products portfolio. It includes a comprehensive embedded software platform delivered for each STM32 series.
   * The CMSIS modules (core and device) corresponding to the ARM(tm) core implemented in this STM32 product.
   * The STM32 HAL-LL drivers, an abstraction layer offering a set of APIs ensuring maximized portability across the STM32 portfolio.
   * The BSP drivers of each evaluation, demonstration or nucleo board provided for this STM32 series.
   * A consistent set of middleware libraries such as RTOS, USB, FatFS, graphics, touch sensing library...
   * A full set of software projects (basic examples, applications, and demonstrations) for each board provided for this STM32 series.

The **STM32CubeL0 MCU Package** projects are directly running on the STM32L0 series boards. You can find in each Projects/*Board name* directories a set of software projects (Applications/Demonstration/Examples).

## Release note

Details about the content of this release are available in the release note [here](https://htmlpreview.github.io/?https://github.com/STMicroelectronics/STM32CubeL0/blob/master/Release_Notes.html).

## How to use

This repository has been created using the `git submodule` command. Please check the instructions below for proper use. Please check also the [notes](README.md#notes) at the end of this section for further information.

1. To **clone** this repository along with the linked submodules, option `--recursive` has to be specified as shown below.

```bash
git clone --recursive https://github.com/STMicroelectronics/STM32CubeL0.git
```

2. To get the **latest updates**, in case this repository is **already** on your local machine, issue the following **two** commands (with this repository as the **current working directory**).

```bash
git pull
git submodule update --init --recursive
```

3. To use the **same firmware version** as the one available on [st.com](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html), issue the command below **after** specifying the targeted `vX.Y.Z` version. This should be done **after** the command(s) indicated in instruction (1) or in instruction (2) above have been successfully executed.

```bash
git checkout vX.Y.Z # Specify the targeted vX.Y.Z version
```

4. To **avoid** going through the above instructions and **directly** clone the same firmware version as the one available on [st.com](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html), issue the command below **after** specifying the targeted `vX.Y.Z` version.

```bash
git clone --recursive  --depth 1 --branch vX.Y.Z https://github.com/STMicroelectronics/STM32CubeL0.git
```

#### Notes

* The latest version of this firmware available on GitHub may be **ahead** of the one available on [st.com](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html) or via [STM32CubeMX](https://www.st.com/en/development-tools/stm32cubemx.html). This is due to the **rolling release** process deployed on GitHub. Please refer to [this](https://github.com/STMicroelectronics/STM32Cube_MCU_Overall_Offer/discussions/21) post for more details.
* Option `--depth 1` specified in instruction (4) above is **not** mandatory. It may be useful to skip downloading all previous commits up to the one corresponding to the targeted version.
* If GitHub "Download ZIP" option is used instead of the `git clone` command, then the different submodules have to be collected and added **manually**.

## Boards available

  * STM32L0
    * [NUCLEO-L010RB](https://www.st.com/en/evaluation-tools/nucleo-l010rb.html)
    * [NUCLEO-L011K4](https://www.st.com/en/evaluation-tools/nucleo-l011k4.html)
    * [NUCLEO-L031K6](https://www.st.com/en/evaluation-tools/nucleo-l031k6.html)
    * [32L0538DISCOVERY](https://www.st.com/en/evaluation-tools/32l0538discovery.html)
    * [NUCLEO-L053R8](https://www.st.com/en/evaluation-tools/nucleo-l053r8.html)
    * [NUCLEO-L073RZ](https://www.st.com/en/evaluation-tools/nucleo-l073rz.html)
    * [STM32L073Z_EVAL](https://www.st.com/en/evaluation-tools/stm32l073z-eval.html)

## Troubleshooting

**Caution** : The issues and the pull-requests are **strictly limited** to submit problems or suggestions related to the software delivered in this repository.

**For any other question** related to the product, the hardware performance or characteristics, the tools, the environment, you can submit it to the **ST Community** on the STM32 MCUs related [page](https://community.st.com/s/group/0F90X000000AXsASAW/stm32-mcus).

## Update 02/01/2024
 * To import STM32 examples into STM32CUBEIDE the user should clone this repo and login in their respective ST account using the ![image] (https://github.com/MaximilianoGraf/STM32CubeL0/assets/73368714/2e64a8dc-bae0-4cc1-a23c-8aaf70e94aea) button.
 * Select the option ![image](https://github.com/MaximilianoGraf/STM32CubeL0/assets/73368714/8e10ca9e-472e-42b7-829e-97d21be988e3) placed in the left side from the Information Center screen. The examples selection window should be opened at this time.
 * Select the right board and desired example, then click on the next button at the bottom.
 * If the legend "Fail to perform local copy" ![image](https://github.com/MaximilianoGraf/STM32CubeL0/assets/73368714/182d20b1-01d8-4ae4-8454-84b2c73dff6e)
appears, this means that the location of the firmware is wrong. Click next
 * In the Firmware Library Package Setup, change the current location to the repo path cloned before. Click on the Firmware Updater link and introduce re right path.
 * In this example the STM32CubeL0 it's used: ![image](https://github.com/MaximilianoGraf/STM32CubeL0/assets/73368714/867af0fd-a694-48d2-887f-13f0a81d21eb)
 * Apply and close
 * Click on finish and that's it.
