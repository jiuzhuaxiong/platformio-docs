..  Copyright (c) 2014-present PlatformIO <contact@platformio.org>
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
       http://www.apache.org/licenses/LICENSE-2.0
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

.. _board_riscv_coreplexip-e51-arty:

E51 Arty (Artix-7) FPGA Dev Kit
===============================

.. contents::

Hardware
--------

Platform :ref:`platform_riscv`: RISC-V is an open, free ISA enabling a new era of processor innovation through open standard collaboration. Born in academia and research, RISC-V ISA delivers a new level of free, extensible software and hardware freedom on architecture, paving the way for the next 50 years of computing design and innovation.

.. list-table::

  * - **Microcontroller**
    - E51
  * - **Frequency**
    - 1500MHz
  * - **Flash**
    - 16MB
  * - **RAM**
    - 256MB
  * - **Vendor**
    - `Xilinx <http://www.xilinx.com/products/boards-and-kits/arty.html?utm_source=platformio&utm_medium=docs>`__


Configuration
-------------

Please use ``coreplexip-e51-arty`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:coreplexip-e51-arty]
  platform = riscv
  board = coreplexip-e51-arty

You can override default E51 Arty (Artix-7) FPGA Dev Kit settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `coreplexip-e51-arty.json <https://github.com/platformio/platform-riscv/blob/master/boards/coreplexip-e51-arty.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:coreplexip-e51-arty]
  platform = riscv
  board = coreplexip-e51-arty

  ; change microcontroller
  board_build.mcu = e51

  ; change MCU frequency
  board_build.f_cpu = 1500000000L

Debugging
---------

:ref:`piodebug` - "1-click" solution for debugging with a zero configuration.

.. warning::
    You will need to install debug tool drivers depending on your system.
    Please click on compatible debug tool below for the further
    instructions and configuration information.

You can switch between debugging :ref:`debugging_tools` using
:ref:`projectconf_debug_tool` option in :ref:`projectconf`.

E51 Arty (Artix-7) FPGA Dev Kit does not have on-board debug probe and **IS NOT READY** for debugging. You will need to use/buy one of external probe listed below.

.. list-table::
  :header-rows:  1

  * - Compatible Tools
    - On-board
    - Default
  * - :ref:`debugging_tool_olimex-arm-usb-tiny-h`
    - 
    - Yes

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_freedom-e-sdk`
      - Open Source Software for Developing on the SiFive Freedom E Platform