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

.. _board_nxplpc_blueboard_lpc11u24:

NGX Technologies BlueBoard-LPC11U24
===================================

.. contents::

Hardware
--------

Platform :ref:`platform_nxplpc`: The NXP LPC is a family of 32-bit microcontroller integrated circuits by NXP Semiconductors. The LPC chips are grouped into related series that are based around the same 32-bit ARM processor core, such as the Cortex-M4F, Cortex-M3, Cortex-M0+, or Cortex-M0. Internally, each microcontroller consists of the processor core, static RAM memory, flash memory, debugging interface, and various peripherals.

.. list-table::

  * - **Microcontroller**
    - LPC11U24
  * - **Frequency**
    - 48MHz
  * - **Flash**
    - 32KB
  * - **RAM**
    - 8KB
  * - **Vendor**
    - `NGX Technologies <https://developer.mbed.org/platforms/BlueBoard-LPC11U24/?utm_source=platformio.org&utm_medium=docs>`__


Configuration
-------------

Please use ``blueboard_lpc11u24`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:blueboard_lpc11u24]
  platform = nxplpc
  board = blueboard_lpc11u24

You can override default NGX Technologies BlueBoard-LPC11U24 settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `blueboard_lpc11u24.json <https://github.com/platformio/platform-nxplpc/blob/master/boards/blueboard_lpc11u24.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:blueboard_lpc11u24]
  platform = nxplpc
  board = blueboard_lpc11u24

  ; change microcontroller
  board_build.mcu = lpc11u24

  ; change MCU frequency
  board_build.f_cpu = 48000000L


Uploading
---------
NGX Technologies BlueBoard-LPC11U24 supports the following uploading protocols:

* ``blackmagic``
* ``jlink``
* ``mbed``

Default protocol is ``mbed``

You can change upload protocol using :ref:`projectconf_upload_protocol` option:

.. code-block:: ini

  [env:blueboard_lpc11u24]
  platform = nxplpc
  board = blueboard_lpc11u24

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

NGX Technologies BlueBoard-LPC11U24 does not have on-board debug probe and **IS NOT READY** for debugging. You will need to use/buy one of external probe listed below.

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