# Ender-3-Max-Neo-Sprite-Pro
Klipper printer settings for Ender 3 Max Neo v4.2.7 board with the Sprite Extruder Pro upgrade. 

Credit goes to ParrotKng for posting the v4.2.2 version on Reddit. https://www.reddit.com/r/klippers/comments/yxd4z7/for_anyone_trying_to_install_fluidd_klipper_on/ <br />
Credit also goes to BotMeka for creating a 3D printed part that allows this to work. https://www.thingiverse.com/thing:5581314 <br />
Credit also goes to bamacups for creating a 3D printed part for the filament sensor. https://www.thingiverse.com/thing:5886875 <br />


Cura Settings:<br />

Start G-Code:<br />
; Ender 3 Max Custom Start G-code
G92 E0 ; Reset Extruder
G28 ; Home all axes
G1 Z2.0 F3000 ; Move Z Axis up little to prevent scratching of Heat Bed
G1 X10.1 Y20 Z0.3 F5000.0 ; Move to start position
G1 X10.1 Y200.0 Z0.3 F1500.0 E15 ; Draw the first line
G1 X10.4 Y200.0 Z0.3 F5000.0 ; Move to side a little
G1 X10.4 Y20 Z0.3 F1500.0 E30 ; Draw the second line
G92 E0 ; Reset Extruder
G1 Z2.0 F3000 ; Move Z Axis up little to prevent scratching of Heat Bed
G1 X5 Y20 Z0.3 F5000.0 ; Move over to prevent blob squish

End G-Code:
G91 ;Relative positioning
G1 E-2 F2700 ;Retract a bit
G1 E-2 Z0.2 F2400 ;Retract and raise Z
G1 X5 Y5 F3000 ;Wipe out
G1 Z10 ;Raise Z more
G90 ;Absolute positioning

G1 X0 Y290 ;Present print
M106 S0 ;Turn-off fan
M104 S0 ;Turn-off hotend
M140 S0 ;Turn-off bed

M84 X Y E ;Disable all steppers but Z

Extruder:
Nozzle Offset X: -5.0mm
