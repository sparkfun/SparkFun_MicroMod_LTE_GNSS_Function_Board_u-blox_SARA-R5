
!!! note

    ### Arduino IDE

    This example assumes you are using the latest version of the Arduino IDE on your desktop. If this is your first time using Arduino IDE and an library, please review the following tutorials.

    - [Installing the Arduino IDE](https://learn.sparkfun.com/tutorials/installing-arduino-ide)
    - [Installing an Arduino Library](https://learn.sparkfun.com/tutorials/installing-an-arduino-library)


    ### Board Definitions

    For the scope of this tutorial, we will be using the [MicroMod ESP32 Processor Board](https://learn.sparkfun.com/tutorials/micromod-esp32-processor-board-hookup-guide/software-setup-and-programming). If you have not installed a board definition before, please review the following tutorial as well.

    - [Installing Board Definitions in the Arduino IDE](https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide)

    ### USB-to-Serial Drivers

    The MicroMod ESP32 Processor Board also uses the CP2104 USB-to-Serial converter (other compatible Processor Boards may require a different driver). Users will need to install the SiLabs CP2104 Driver, which can be found here: [USB to UART Bridge VCP Driver](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers#software). Make sure to manually install the driver for the CP2104 with the following instructions. The driver that Windows auto-installs will not work with the auto-reset circuit on the board and cause serial uploads to fail.

    - [Windows VCP Driver (ZIP)](https://cdn.sparkfun.com/assets/learn_tutorials/8/5/2/CP210x_Universal_Windows_Driver.zip)
    - [MAC OSX VCP Driver (ZIP)](https://www.silabs.com/documents/public/software/Mac_OSX_VCP_Driver.zip)

    If applicable, make sure you are using the proper driver files for your CPU architecture. This is usually indicated by a folder or file name with "x86" for 32-bit processors or "x64" for 64-bit processors.

The SparkFun u-blox SARA-R5 Arduino Library provides a quick way to interact with the interfaces on the MicroMod LTE GNSS Function Board. Install the library through the Arduino Library Manager tool by searching for "**SparkFun u-blox SARA-R5**". Users who prefer to manually install the library can get it from the [GitHub Repository](https://github.com/sparkfun/SparkFun_u-blox_SARA-R5_Arduino_Library) or download the .ZIP by clicking the button below:

<div style="text-align: center"><a href="https://github.com/sparkfun/SparkFun_u-blox_SARA-R5_Arduino_Library/archive/refs/heads/master.zip" class="md-button">SparkFun SARA-R5 Arduino Library (ZIP)</a></div>



The library primarily works by associating a selection of AT Commands from the [Command Set Manual](https://cdn.sparkfun.com/assets/b/6/2/4/5/SARA-R5_ATCommands__UBX-19047455_.pdf) with standard Arduino functions to run automatically in a sketch. View the full list of AT Commands included in this library (along with all other available functions) in the [header file](https://github.com/sparkfun/SparkFun_u-blox_SARA-R5_Arduino_Library/blob/master/src/SparkFun_u-blox_SARA-R5_Arduino_Library.h). The list of included [AT Commands starts on line 93](https://github.com/sparkfun/SparkFun_u-blox_SARA-R5_Arduino_Library/blob/main/src/SparkFun_u-blox_SARA-R5_Arduino_Library.h#L93).

!!!note
    When using the MicroMod ESP32 Processor Board with the  **SparkFun_u-blox_SARA-R5_Arduino_Library** make sure to include the following line of code in the `setup()` function to enable the voltage regulator:

    <pre><code class="language-cpp">&nbsp;&nbsp;&nbsp;&nbsp;pinMode(PWM1, INPUT_PULLUP); // EN on F0 when using the ESP32 Processor Board</code></pre>
