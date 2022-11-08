### ESP8266 CONNECTION (USING ESP-01)

1- Connection

- Flash the following to nano

```
int ch_pd = 3;
int io0 = 2;

void setup() {
  pinMode(ch_pd, OUTPUT);
  pinMode(io0, OUTPUT);
  digitalWrite(io0,LOW);
  digitalWrite(ch_pd, LOW);
  delay(1000);
  digitalWrite(ch_pd, HIGH);
}

void loop()
{
      
}
```

- Connection

- nano gnd -> esp8266 gnd + esp8266 rst + esp8266 gpio0
- nano 3.3 -> esp8266 3.3v
- nano rx -> esp8266 rx
- nano tx -> esp8266 tx

### FIRMWARE UPDATE PROCEDURE

- Open flash_download_tool_v3.8.5, select developer and esp8266
- Refer to MEM-MAP.PNG for every bin location and check every box
- Select 8M as flash size (may be different on yours, uncheck all to display the info from the board)
- click start and wait for 3 seconds, then unplug the RST from GND.
- wait to finish :)
