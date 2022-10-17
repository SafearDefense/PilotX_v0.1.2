# PilotX_v0.1.2
Multi-vehicle Ground Control Station Software


**Download the software here** : https://github.com/SafearDefense/PilotX_v0.1.2/releases/tag/v0.1.2

#1
PilotX v0.1.2 is a initial interface software of a long vision Flight Controller & Mission Planning Technologies. Though PilotX v0.1.2 is in its initial phase, yet it is equipped with numerous advanced features. The most interactive feature of this software is that it comes with dedicated interfaces for
UAV (Unmanned Aerial Vehicles) & UGV (Unmanned Ground Vehicles). PilotX is developed with a long term vision of creating a full-fledged autopilot system for almost all vehicles including Underwater Vehicles and robots.

This documentation will keep developing over time with every new feature being added into the software.

PilotX is a highly version controlled system, therefore its necessary to understand the naming-tree for our versions.

V0.1.2 = BASE VERSION (=0) MAJOR UPDATES (=1) MINOR UPDATES (=2)

V0.1.2 beta = [ BASE VERSION (=0) MAJOR UPDATES (=1) MINOR UPDATES (=2) ] but is an unstable release and is still under development

#2
Type Of Updates:

Any minor update would be regarding the bugs addressed or found, enhancing the features or any little new feature being added to the software. 
All major updates would come with a new look, new design (but same backend principle) and new and more advanced features.
Our team of developers continiously works on developing and testing new versions every now and then, and whenever we feel we should present you something, we release it as a beta version to get feedbacks from our users.

#3
Understand PilotX:

HUD: HUD or Head Up Display is a feature of any unmanned ground vehicle's control station that provides the vehicle controller with an overview of what is happening with and around the vehicle. PilotX's HUD is the main interface which open's by default on opening the software. 

PilotX has two HUD interfaces, first for the Aerial Vehicles, and second for the Ground Vehicles. The interface can be changed using Drop Down Menu given below the data panel. You can change the interface at any point of time within the software. If you are a multi-vehicle developer, then you can easily switch between both interfaces quickly. Both interfaces have their own display features that we will discuss one by one.

Interface 1: UAV (Unmanned Aerial Vehicle) Interface

UAV Interface consists of:
a. Attitude Indicator
b. Data Panel
c. Log & Simulation Panel
d. Interface & COM Selection Panel
e. Critical Warning Indicators
f. Dial Gauges
g. Compass
h. Transmitter Channel Indicator
i. Time of Flight

Let us understand and explore each feature one by one:

A. Attitude Indicator: Attitude indicator displays a aircraft from rear view as if POV is following the aircraft from the tail. Attitude indicator displays the roll & pitch as real time visualization. Attitude indicator not only displays real time flight attitude but can also show you simulations from a previous flight. Attitude Indicator has a large text warning system for roll error and pitch error which is designed for pilots flying the aircraft and keeping an eye on the Ground Station as well. However, Attitude Indicator's warning system are displayed by default, which can be set in the settings and analysis panel.

B. Data Panel: Data Panel is more for data geeks and for users who trust raw data more over publisher's conversions. Data panel displays 12 different types of raw data which includes: 
Raw X Rotation (ax_raw), Raw Y Rotation (ay_raw), Raw Z Rotation (az_raw), Raw X Angular Acceleration (gx_raw), Raw Y Angular Acceleration (gy_raw), Raw Z Angular Acceleration (gz_raw), Roll Angle, Pitch Angle, Humidity, Altitude, Temperature and Servo 1 to Servo 6 Values where Servo 1, 2, 3 are connected with Aileron, Elevator and Rudder, rest 3 Servo motors from Servo 4 to 6 are NULL and can be used for any purpose.

C: Log & Simulation Panel: This panel is dedicated for Creating Log Files of the flight and simulating them. Create Log Button starts creating a log in the ".txt" format. Stop Logging will stop the logging immediately. Each log file is saved with the name of "PilotX Log File (date of log run) (time of log run).txt". PilotX Software comes with 3 sample log files (Sample Log 1.txt, Sample Log 2.txt, Sample Log 3.txt) for ease of understanding the software and its simulation feature. Log files can be located in the location where you have unzipped PilotX's Tar/Zip file. 
Simulation Button opens a file selection menu which by default the Log File Location. If you select any of the Log Files (pre-existing or user created log). 
Once a valid log file is selected, a voice command initiates the simulation and you can visualize the log in real time as if a real flight. While simulation is running you can see activity all over the interface which is re-running the complete flight.

D: Interface & COM Selection Panel: COM Selection panel can be used to select the COM Port through which the vehicle is connected. Currently only COM Ports (USB Data) & Telemetry data is supported. USB Data can be easily used by connecting any standard microcontroller. Whereas for telemetry NRFL101 Antennas and all long range antennas can be used for data transmission. Interface selection panel gives you the access to switch between UGV and UAV interfaces instantaneously.

E. Critical Warning Indicator: These indicators are designed to let the pilot know if the roll angle or pitch angle has exceeded the normal limits. Currently the indicators warn at roll or pitch angle greater than 45 degrees. However in future versions this threshold value can be set by the user.

F. Dial Gauges: Dial Gauges indicate the value of Altitude, Roll & Pitch Angle in an more interactive way.

G. Compass: Compass defines the direction of heading.

H: Transmitter Channel Indicator: There are 6 channels whose real time value is displayed on the interface, named CH1 to CH6. Any channel can be used for any purpose. Currently software supports only 6 channels but in future versions number of channels and their specific roles will be extended to 16.

I. Active Flight Time: The time of flight is a dual indicator. It displays the total time for which software is ON and additionally can be used for the total duration of flight.

#4
Interface 2: UGV (Unmanned Ground Vehicles) Interface

UGV Interface consists of:
a. Roll Indicator
b. Climb Indicator
c. Obstacle Detection Map
d. Robotic Arm Status
e. Data Panel
f. Log & Simulation Panel
g. Interface & COM Selection Panel
h. Critical Warning Indicators
i. Dial Gauges
j. Compass
k. Transmitter Channel Indicator
l. Active Driving Time

Let us understand and explore each feature one by one:

A. Roll Indicator: It displays the left and right tilt in the vehicle as if POV is following from the rear side.

B. Climb Indicator: It displays how steep is the ground on which the vehicle is standing. This allows the vehicle controller to understand when and how much to give the race.

C: Obstacle Detection Map: This map is more like a radar, if you are using a ultrasonic sensor, LIDAR or any such obstacle mapping device, the obstacles can be always seen on this map. This allows the vehicle controller to understand the enviroment and take necessary actions.

D: Robotic Arm Status: If your UGV comes with a robotic arm on it, that can be visualized using this block. Currently the system supports only 2 branches of arm. This allows the vehicle controller to more clearly pick and place objects.

B. Data Panel: Data Panel is more for data geeks and for users who trust raw data more over publisher's conversions. Data panel displays 12 different types of raw data which includes: 
Raw X Rotation (ax_raw), Raw Y Rotation (ay_raw), Raw Z Rotation (az_raw), Raw X Angular Acceleration (gx_raw), Raw Y Angular Acceleration (gy_raw), Raw Z Angular Acceleration (gz_raw), Roll Angle, Climb Angle, Humidity, Altitude, Temperature and Servo 1 to Servo 6 Values where Servo 1, 2, 3, 4 are connected with 4 Motors (you can use less than 4 motors as well), rest 3 Servo motors from Servo 4 to 6 are NULL and can be used for any purpose (such as robotic arm).

C: Log & Simulation Panel: This panel is dedicated for Creating Log Files of the drive and simulating them. Create Log Button starts creating a log in the ".txt" format. Stop Logging will stop the logging immediately. Each log file is saved with the name of "PilotX Log File (date of log run) (time of log run).txt". PilotX Software comes with 3 sample log files (Sample Log 1.txt, Sample Log 2.txt, Sample Log 3.txt) for ease of understanding the software and its simulation feature. Log files can be located in the location where you have unzipped PilotX's Tar/Zip file. 
Simulation Button opens a file selection menu which by default the Log File Location. If you select any of the Log Files (pre-existing or user created log). 
Once a valid log file is selected, a voice command initiates the simulation and you can visualize the log in real time as if a real drive. While simulation is running you can see activity all over the interface which is re-running the complete drive session.

D: Interface & COM Selection Panel: COM Selection panel can be used to select the COM Port through which the vehicle is connected. Currently only COM Ports (USB Data) & Telemetry data is supported. USB Data can be easily used by connecting any standard microcontroller. Whereas for telemetry NRFL101 Antennas and all long range antennas can be used for data transmission. Interface selection panel gives you the access to switch between UGV and UAV interfaces instantaneously.

E. Critical Warning Indicator: These indicators are designed to let the pilot know if the roll angle or climb angle has exceeded the normal limits. Currently the indicators warn at roll or climb angle greater than 45 degrees. However in future versions this threshold value can be set by the user.

F. Dial Gauges: Dial Gauges indicate the value of Altitude, Roll & Climb Angle in an more interactive way.

G. Compass: Compass defines the direction of heading.

H: Transmitter Channel Indicator: There are 6 channels whose real time value is displayed on the interface, named CH1 to CH6. Any channel can be used for any purpose. Currently software supports only 6 channels but in future versions number of channels and their specific roles will be extended to 16.

I. Active Driving Time: It is a dual indicator. It displays the total time for which software is ON and additionally can be used for the total duration of driving.

#5
Settings & Analysis

Settings and data analysis tab is divided into two sections. The first section is for settings, the second section is for data analysis. 

Settings:

Settings section allows you to tune your Compass, Gyroscopic Values, PID Tuning etc. However this panel is deactivated for this version as tuning can be done in user's local hardware (microcontroller).
Apart from these control parameters, PilotX also allows you to set some App Features such as:

A. Default COM Port: You can pre-set your default COM Port and next time when you restart the tab, you will be able to see new settings applied.

B. Default Interface: You can set the default interface depending on the type of interface you are developing. When not set, default interface is for UAVs however it can be changed for UGVs by changing it in settings.

C: Auto-logging: By default auto-logging feature is OFF, but can be turned ON for all upcoming sessions of software using settings.

D: Warnings: Attitude indicator has a warning feature which displays roll or pitch error for convenience of Pilot/Controller. But by default the warning system is OFF but can be set to ON using this setting.

#6
Analysis:

Analysis feature allows user to visualise the flight logs in form of graphs. This can be useful when flights/drivings are done for the purpose of research and development of a vehicle or aircraft. This can also be useful for data extraction and later analysing it. 

Analysis feature requires you to select a LOG File and once selected it displays all data available in form of a common graph with different colored lines for different variables. However the variable that has to be included in the graph can be selected to deselected from below. After selecting or deselecting the variables, user must click on "Refresh" button to see the changes.

#7
Connecting your own Hardware with PilotX Software

PilotX supports almost all standard microcontrollers. All microcontrollers can be easily connected over USB (for tethered connections). For logn range connections, Telemetry can be used instead of COM Ports.

What to do?
Upload your flight controlling code or rover/UGV code onto your microcontroller (say Arduino UNO). Along with the code, you must send some data over Serial at baud rate of 38400. 

For example: You wish to see ax_raw, ay_raw, az_raw on the PilotX Software, then your code must write these values over the serial monitor. 

This can be done simply by adding:

Serial.print(ax_raw);
Serial.print(',');
Serial.print(ay_raw);
Serial.print(',');
Serial.println(az_raw); 

All values that you wish to display on the PilotX software should be printed in a loop in a single line.

6000, 4000, 3000
8000, 2000, 1400

Each line should contain all values that you wish to display on PilotX seperated by commas.

The sequence of PilotX interpreting the serial data is as follows:

ax_raw, ay_raw, az_raw, gx_raw, gy_raw, gz_raw, heading, air_pressure, humidity, Servo Angle 1, Servo Angle 2, Servo Angle 3, Servo Angle 4, Servo Angle 5, Servo Angle 6, Transmitter CH1 Value,  Transmitter CH2 Value, Transmitter CH3 Value, Transmitter CH4 Value, Transmitter CH5 Value, Transmitter CH6 Value.

Incase if you wish to display only ax_raw & Servo angle 1 in PilotX, then you can print values for all other parameters as 0. This can be done using;

Serial.print(ax_raw);
Serial.print(',');
Serial.print("0");
Serial.print(',');
.................
.................
.................
Serial.print(Servo Angle 1);
Serial.print(',');
Serial.print("0");
Serial.print(',');
.................


