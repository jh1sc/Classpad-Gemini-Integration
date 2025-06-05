# Basic Serial Control
**BASED OFF [serial.hpp](../hollyhock-2/sdk/include/sdk/os/serial.hpp)**

```cpp
void Serial::begin()
```
- Purpose: Initializes serial communication
- Default baud rate: 115200
- Found in: `sdk/os/serial.hpp`
- Example:
```cpp
Serial.begin();  // Start serial communication
```

```cpp
void Serial::end()
```
- Purpose: Terminates serial communication
- Found in: `sdk/os/serial.hpp`
- Example:
```cpp
Serial.end();  // Stop serial communication
```

#### Data Transmission
```cpp
size_t Serial::write(uint8_t byte)
size_t Serial::write(const char* str)
size_t Serial::write(const uint8_t* buffer, size_t size)
```
- Purpose: Sends data through serial port
- Returns: Number of bytes written
- Found in: `sdk/os/serial.hpp`
- Examples:
```cpp
Serial.write('A');           // Send single byte
Serial.write("Hello");       // Send string
uint8_t buf[3] = {1,2,3};
Serial.write(buf, 3);        // Send buffer
```

#### Data Reception
```cpp
int Serial::available()
```
- Purpose: Checks for available data
- Returns: Number of bytes available to read
- Found in: `sdk/os/serial.hpp`
- Example:
```cpp
if(Serial.available() > 0) {
    // There is data to read
}
```

```cpp
int Serial::read()
```
- Purpose: Reads one byte of data
- Returns: -1 if no data, 0-255 for received byte
- Found in: `sdk/os/serial.hpp`
- Example:
```cpp
if(Serial.available()) {
    int incoming = Serial.read();
}
```