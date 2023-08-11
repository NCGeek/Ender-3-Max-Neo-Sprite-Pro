# Ender-3-Max-Neo-Sprite-Pro
Klipper printer settings for Ender 3 Max Neo v4.2.7 board with the Sprite Extruder Pro upgrade. 

Credit goes to ParrotKng for posting the v4.2.2 version on Reddit. https://www.reddit.com/r/klippers/comments/yxd4z7/for_anyone_trying_to_install_fluidd_klipper_on/ <br />
Credit also goes to BotMeka for creating a 3D printed part that allows this to work. https://www.thingiverse.com/thing:5581314 <br />
Credit also goes to bamacups for creating a 3D printed part for the filament sensor. https://www.thingiverse.com/thing:5886875 <br />


Cura Settings:<br />

Start G-Code:<br />
; Ender 3 Max Custom Start G-code<br />
G92 E0 ; Reset Extruder<br />
G28 ; Home all axes<br />
G1 Z2.0 F3000 ; Move Z Axis up little to prevent scratching of Heat Bed<br />
G1 X10.1 Y20 Z0.3 F5000.0 ; Move to start position<br />
G1 X10.1 Y200.0 Z0.3 F1500.0 E15 ; Draw the first line<br />
G1 X10.4 Y200.0 Z0.3 F5000.0 ; Move to side a little<br />
G1 X10.4 Y20 Z0.3 F1500.0 E30 ; Draw the second line<br />
G92 E0 ; Reset Extruder<br />
G1 Z2.0 F3000 ; Move Z Axis up little to prevent scratching of Heat Bed<br />
G1 X5 Y20 Z0.3 F5000.0 ; Move over to prevent blob squish<br />

End G-Code:<br />
G91 ;Relative positioning<br />
G1 E-2 F2700 ;Retract a bit<br />
G1 E-2 Z0.2 F2400 ;Retract and raise Z<br />
G1 X5 Y5 F3000 ;Wipe out<br />
G1 Z10 ;Raise Z more<br />
G90 ;Absolute positioning<br />

G1 X0 Y290 ;Present print<br />
M106 S0 ;Turn-off fan<br />
M104 S0 ;Turn-off hotend<br />

Additional Information:<br />
https://github.com/Jyers/Marlin/discussions/814<br />
M140 S0 ;Turn-off bed<br />

M84 X Y E ;Disable all steppers but Z<br />

Extruder:
Nozzle Offset X: -5.0mm
