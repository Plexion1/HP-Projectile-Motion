EXPORT Projectile_Motion()
BEGIN
LOCAL Launch_Velocity, Launch_Angle, Launch_Height, Final_Height, X_Position, Time, g;
// Acceleration due to gravity
g := 9.803; // Default value for Earth's gravity in m/s²

// Input variables
Launch_Velocity := 0; // Initial launch velocity in m/s
Launch_Angle := 0; // Launch angle in degrees
Launch_Height := 0; // Launch height in meters
Final_Height := 0; // Final height in meters
X_Position := 0; // Final X position in meters

INPUT({Launch_Velocity, Launch_Angle, Launch_Height, Final_Height, g},
"Projectile Motion Inputs",
{"Initial Velocity (m/s)", "Launch Angle (degrees)", "Launch Height (meters)", "Final Height (meters)", "Gravity (m/s²)"},
{"Enter the initial launch velocity (m/s)",
"Enter the launch angle (degrees)",
"Enter the launch height (meters)",
"Enter the final height (meters)",
"Enter the acceleration due to gravity (m/s²)"});

Time := (-Launch_Velocity * sin(Launch_Angle) - sqrt((Launch_Velocity * sin(Launch_Angle))^2 - 4 * (0.5 * -g) * (Launch_Height - Final_Height))) / -g;

X_Position := Launch_Velocity * cos(Launch_Angle) * Time;

// Output the results
MSGBOX("Results:" +
"\nFinal X position: " + X_Position + " meters" +
"\nTime of flight: " + Time + " seconds");
END;