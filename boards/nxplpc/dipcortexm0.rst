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

.. _board_nxplpc_dipcortexm0:

Solder Splash Labs DipCortex M0
===============================

.. contents::

Hardware
--------

Platform :ref:`platform_nxplpc`: The NXP LPC is a family of 32-bit microcontroller integrated circuits by NXP Semiconductors. The LPC chips are grouped into related series that are based around the same 32-bit ARM processor core, such as the Cortex-M4F, Cortex-M3, Cortex-M0+, or Cortex-M0. Internally, each microcontroller consists of the processor core, static RAM memory, flash memory, debugging interface, and various peripherals.

.. list-table::

  * - **Microcontroller**
    - LPC11U24
  * - **Frequency**
    - 50MHz
  * - **Flash**
    - 32KB
  * - **RAM**
    - 8KB
  * - **Vendor**
    - `Solder Splash Labs <https://developer.mbed.org/platforms/DipCortex-M0/?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``dipcortexm0`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:dipcortexm0]
  platform = nxplpc
  board = dipcortexm0

You can override default Solder Splash Labs DipCortex M0 settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `dipcortexm0.json <https://github.com/platformio/platform-nxplpc/blob/master/boards/dipcortexm0.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:dipcortexm0]
  platform = nxplpc
  board = dipcortexm0

  ; change microcontroller
  board_build.mcu = lpc11u24

  ; change MCU frequency
  board_build.f_cpu = 50000000L


Uploading
---------
Solder Splash Labs DipCortex M0 supports the following uploading protocols:

* ``blackmagic``
* ``jlink``
* ``mbed``

Default protocol is ``mbed``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:dipcortexm0]
  platform = nxplpc
  board = dipcortexm0

  upload_protocol = mbed

Debugging
---------

:ref:`piodebug` - "1-click" solution for debugging with a zero configuration.

.. warning::
    You will need to install debug tool drivers depending on your system.
    Please click on compatible debug tool below for the further
    instructions and configuration information.

You can switch between debugging :ref:`debugging_tools` using
:ref:`projectconf_debug_tool` option in :ref:`projectconf`.

Solder Splash Labs DipCortex M0 does not have on-board debug probe and **IS NOT READY** for debugging. You will need to use/buy one of external probe listed below.

.. list-table::
  :header-rows:  1

  * - Compatible Tools
    - On-board
    - Default
  * - :ref:`debugging_tool_blackmagic`
    - 
    - Yes
  * - :ref:`debugging_tool_jlink`
    - 
    - 

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_mbed`
      - Arm Mbed OS is a platform operating system designed for the internet of things