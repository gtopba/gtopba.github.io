.. title: Airbag crash data reset
.. slug: airbag-crash-data-reset
.. date: 2018-06-16 10:23:07 UTC+07:00
.. tags: embedded, EEPROM
.. category: hardware
.. link: 
.. description: 
.. type: text

	
After a collision and the airbags are deployed, the airbag controller stores information such as speed, RPM, seat belt, accelerometer, pre-tensioner that can be used for investigation. These crash data need to be replaced, if the vehicle is rebuilt. Otherwise the airbag light will stay solid and the vehicle might not perform correctly. The crash data is stores in the EEPROM chip, which can be read/write via a cheap programmer. A virgin data is copied from another vehicle's controller, which then will be used to replaced the crash data inside the EEPROM.

.. figure:: /pic/airbag/L56R_EEPROM.jpg
   :align: center
   :height: 1440
   :width: 1079
   :scale: 40
   
   L56R EEPROM
	
The closest datasheet to the L56R EEPROM I found was BR93L56F, the Microwire BUS 2Kbit(128x16bit) EEPROM. 

.. figure:: /pic/airbag/Pin_configurations.PNG
   :align: center
   :height: 438
   :width: 1084
   :scale: 50

   Pin configurations
	
The programmer is MiniPro TL866A from Aliexpress. Reading the EEPROM in circuit using SOP8 clip was not successful even the crystal was shorted out. So the EEPROM has to be removed from the board to be able to read/write with the SOP8 socket.

.. figure:: /pic/airbag/programer.jpg
   :align: center
   :height: 1080
   :width: 1440
   :scale: 40
   
   The programmer with SOP8 socket
	
The virgin data is copied from the good EEPROM and replaced into the bad EEPROM.

.. figure:: /pic/airbag/good-bad-board.jpg
   :align: center
   :height: 1079
   :width: 1167
   :scale: 40
   
   Copying good data to replace crash data.
	
Connect the programmer to a computer and open the software MiniPro Programmer. Select IC the click Read

.. figure:: /pic/airbag/MiniPro.PNG

	Select IC and Read
	
Successfully reading the EEPROM from the good board.

.. figure:: /pic/airbag/MiniPro_Read.PNG

	Read success
	
Read several time to make sure the read data is correct. Insert the bad EEPROM to the programmer and click Program

.. figure:: /pic/airbag/MiniPro_Data.PNG

	Good data ready for writing into bad EEPROM
	
Programming successful!! Read data back to verify the data is all correct. Install the EEPROM back to the board

.. figure:: /pic/airbag/MiniPro_Write.PNG

	Programming successful
	
After installing the controller back to the vehicle, the airbag light should now turned off.
