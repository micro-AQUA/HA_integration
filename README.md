# HA_integration
This integrations allow to connect microAQUA device to the Home Asystent as a TCP sensor.
 
With this integration fallowing entieties are prowided: 

...tbc

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
  4. Edit IP, Port, and Payload to the values specific to your microAQUA device.
      
      All parameters can be read from the menu of your device.
      
      
 # Adding another microAQUA device.   
 
 1. To add second microAQUA device you need to opnen each form the listed files: 
    - secrets.yaml
    - microaqua/uaqua_automations.yaml
    - microaqua/uaqua_input_number.yaml
    - microaqua/uaqua_sensor.yaml
    - microaqua/uaqua_shell_command.yaml
    - microaqua/uaqua_switch.yaml
    
 2. In each file you need to find section: 
 ```yaml
#---------------------------------------------------#
#           microAQUA 2'nd DEVICE SECTION           #
#---------------------------------------------------#
#                                                   #
#     uncomment code in this section to add 2'nd    #
#           microAQUA device to the system          #
#                                                   #
#       To do this ,select configuration code       #
#       in this section and press 'Ctrl' + '/'      #
#---------------------------------------------------#
  ```
  and uncomment yaml code iside of this section.
 
  End of the section is marked by:
 ```yaml
#---------------------------------------------------#
#        END microAQUA 2'nd DEVICE SECTION          #
#---------------------------------------------------#
  ```
3. IMPORTANT

   In file uaqua_sensor.yaml there are two such sections for each device. 
   In this case, for this file its necessary to uncoment code in two places.
 
  
    
    
