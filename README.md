# HA_integration
# Custom Component Installation
  1. Copy the microaqua folder to your own hassio /config folder
  
  3. In your configuration.yaml add the following:
   ```yaml
   #---------------------------------------#
   #       microAQUA integration           #
   #---------------------------------------#
   sensor more: !include microaqua/uaqua_sensor.yaml
   switch more: !include microaqua/uaqua_switch.yaml
   automation more: !include microaqua/uaqua_automations.yaml
   shell_command: !include microaqua/uaqua_shell_command.yaml
   input_number: !include microaqua/uaqua_input_number.yaml
   ```
  3. In your secrets.yaml add the following:
  ```yaml
  #---------------------------------------#
  #       microAQUA integration           #
  #---------------------------------------#

  microAQUA_1_IP: 192.168.0.0
  microAQUA_1_port: 1234
  microAQUA_1_payload: "AT+TCPSCP?\r\n"
  ```
  4. Edit IP port and paylod to the values specific to your microAQUA device.
      
      All parameters can be read from the menu of your device.
      In the file added to this project you can find correctly filled 
  
    
    
