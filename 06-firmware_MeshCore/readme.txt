
;add \variants\heltec_v3\target.h

#include <helpers/radiolib/CustomSX1268Wrapper.h>

;add \variants\heltec_v3\platformio.ini

[env:Heltec_v3_SX1268_repeater]
extends = Heltec_lora32_v3
build_flags =
  ${Heltec_lora32_v3.build_flags}
  -D USE_SX1268
  -D RADIO_CLASS=CustomSX1268
  -D WRAPPER_CLASS=CustomSX1268Wrapper
  -D DISPLAY_CLASS=SSD1306Display
  -D ADVERT_NAME='"MTL-1 433Mhz Repeater"'
  -D ADVERT_LAT=0.0
  -D ADVERT_LON=0.0
  -D ADMIN_PASSWORD='"password"'
  -D MAX_NEIGHBOURS=50
;  -D MESH_PACKET_LOGGING=1
;  -D MESH_DEBUG=1
  -D LORA_FREQ=433.0
  -D LORA_TX_POWER=12
build_src_filter = ${Heltec_lora32_v3.build_src_filter}
  +<helpers/ui/SSD1306Display.cpp>
  +<../examples/simple_repeater>
lib_deps =
  ${Heltec_lora32_v3.lib_deps}
  ${esp32_ota.lib_deps}
  bakercp/CRC32 @ ^2.0.0

[env:Heltec_v3_SX1268_repeater_bridge_rs232]
extends = Heltec_lora32_v3
build_flags =
  ${Heltec_lora32_v3.build_flags}
  -D USE_SX1268
  -D RADIO_CLASS=CustomSX1268
  -D WRAPPER_CLASS=CustomSX1268Wrapper
  -D DISPLAY_CLASS=SSD1306Display
  -D LORA_FREQ=433.0
  -D LORA_TX_POWER=12
  -D ADVERT_NAME='"MTL-1 UART Bridge"'
  -D ADVERT_LAT=0.0
  -D ADVERT_LON=0.0
  -D ADMIN_PASSWORD='"password"'
  -D MAX_NEIGHBOURS=50
  -D WITH_RS232_BRIDGE=Serial2
  -D WITH_RS232_BRIDGE_RX=5
  -D WITH_RS232_BRIDGE_TX=6
;  -D BRIDGE_DEBUG=1
;  -D MESH_PACKET_LOGGING=1
;  -D MESH_DEBUG=1
build_src_filter = ${Heltec_lora32_v3.build_src_filter}
  +<helpers/bridges/RS232Bridge.cpp>
  +<helpers/ui/SSD1306Display.cpp>
  +<../examples/simple_repeater>
lib_deps =
  ${Heltec_lora32_v3.lib_deps}
  ${esp32_ota.lib_deps}

[env:Heltec_v3_SX1268_repeater_bridge_espnow]
extends = Heltec_lora32_v3
build_flags =
  ${Heltec_lora32_v3.build_flags}
  -D RADIO_CLASS=CustomSX1268
  -D WRAPPER_CLASS=CustomSX1268Wrapper
  -D DISPLAY_CLASS=SSD1306Display
  -D LORA_FREQ=433.0
  -D LORA_TX_POWER=12
  -D DISPLAY_CLASS=SSD1306Display
  -D ADVERT_NAME='"MTL-1 ESPNow Bridge"'
  -D ADVERT_LAT=0.0
  -D ADVERT_LON=0.0
  -D ADMIN_PASSWORD='"password"'
  -D MAX_NEIGHBOURS=50
  -D WITH_ESPNOW_BRIDGE=1
;  -D BRIDGE_DEBUG=1
;  -D MESH_PACKET_LOGGING=1
;  -D MESH_DEBUG=1
build_src_filter = ${Heltec_lora32_v3.build_src_filter}
  +<helpers/bridges/ESPNowBridge.cpp>
  +<helpers/ui/SSD1306Display.cpp>
  +<../examples/simple_repeater>
lib_deps =
  ${Heltec_lora32_v3.lib_deps}
  ${esp32_ota.lib_deps}

[env:Heltec_v3_SX1268_companion_radio_usb]
extends = Heltec_lora32_v3
build_flags =
  ${Heltec_lora32_v3.build_flags}
  -I examples/companion_radio/ui-new
  -D RADIO_CLASS=CustomSX1268
  -D WRAPPER_CLASS=CustomSX1268Wrapper
  -D DISPLAY_CLASS=SSD1306Display
  -D LORA_FREQ=433.0
  -D LORA_TX_POWER=12
  -D MAX_CONTACTS=350
  -D MAX_GROUP_CHANNELS=40
  -D DISPLAY_CLASS=SSD1306Display
; NOTE: DO NOT ENABLE -->  -D MESH_PACKET_LOGGING=1
; NOTE: DO NOT ENABLE -->  -D MESH_DEBUG=1
build_src_filter = ${Heltec_lora32_v3.build_src_filter}
  +<helpers/ui/SSD1306Display.cpp>
  +<helpers/ui/MomentaryButton.cpp>
  +<../examples/companion_radio/*.cpp>
  +<../examples/companion_radio/ui-new/*.cpp>
lib_deps =
  ${Heltec_lora32_v3.lib_deps}
  densaugeo/base64 @ ~1.4.0

[env:Heltec_v3_SX1268_companion_radio_ble]
extends = Heltec_lora32_v3
build_flags =
  ${Heltec_lora32_v3.build_flags}
  -I examples/companion_radio/ui-new
  -D RADIO_CLASS=CustomSX1268
  -D WRAPPER_CLASS=CustomSX1268Wrapper
  -D DISPLAY_CLASS=SSD1306Display
  -D LORA_FREQ=433.0
  -D LORA_TX_POWER=12
  -D MAX_CONTACTS=350
  -D MAX_GROUP_CHANNELS=40
  -D DISPLAY_CLASS=SSD1306Display
  -D BLE_PIN_CODE=123456   ; dynamic, random PIN
  -D AUTO_SHUTDOWN_MILLIVOLTS=3400
  -D BLE_DEBUG_LOGGING=1
  -D OFFLINE_QUEUE_SIZE=256
;  -D MESH_PACKET_LOGGING=1
;  -D MESH_DEBUG=1
build_src_filter = ${Heltec_lora32_v3.build_src_filter}
  +<helpers/ui/SSD1306Display.cpp>
  +<helpers/ui/MomentaryButton.cpp>
  +<helpers/esp32/*.cpp>
  +<../examples/companion_radio/*.cpp>
  +<../examples/companion_radio/ui-new/*.cpp>
lib_deps =
  ${Heltec_lora32_v3.lib_deps}
  densaugeo/base64 @ ~1.4.0




