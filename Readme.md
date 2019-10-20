# Interfaces with TI's HDC1080 temperature and humidity sensor
Reads temperature and humidity from the HDC1080 sensor by Texas Instruments. Also allows readout of MfgID, DeviceID, and SerialID.

# Methods:

#### `HDC1080()`

Constructor.

**IMPORTANT NOTE** - currently works for ESP8266 only due to specifics of Wire library.

#### `void get_serial_id(unsigned int* serial_id)`

Get serial number of HDC1080. Arguments are:
- `serial_id` ... Pointer to array of unsigned ints of length 3. Serial number will be written into this array.

#### `unsigned int get_mfg_id()`

Get manufacturer ID.

#### `unsigned int get_device_id()`

Get device ID.

#### `void read(float* temperature, float* humidity)`

Trigger measurements and retrieve temperature and humidity values. Arguments:
- `temperature` ... Pointer to float variable to store temperature value in.
- `humidity` ...  Pointer to float variable to store humidity value in.
