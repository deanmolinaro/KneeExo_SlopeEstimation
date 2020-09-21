1. Right commanded torque (Nm)
2. Right encoder angle (deg)
3. Left commanded torque (Nm)
4. Left encoder angle (deg)
5. Left encoder velocity (deg/s)
6. Right encoder velocity (deg/s)
7. Right assistance state (5 - early stance, 10 - late stance, 15 - ealy swing, 20 - late swing)
8. Left assistance state (5 - early stance, 10 - late stance, 15 - ealy swing, 20 - late swing)
9. Loop time (s)
10. Right FSR (binary)
11. Left FSR (binary)
12-17. Right shank IMU (x,y,z acc and x,y,z gyro - sequencially)
18-23. Right thigh IMU (x,y,z acc and x,y,z gyro - sequencially)
24-29. Left thigh IMU (x,y,z acc and x,y,z gyro - sequencially)
30-35. Left shank IMU (x,y,z acc and x,y,z gyro - sequencially)
36. Right gait cycle stamp (1 - start of a gait cycle, 0 - none)
37. Left gait cycle stamp (1 - start of a gait cycle, 0 - none)

% note: use the following lines of code to detect the indices for heel_contacts,

rightHc = find(diff(read(:,36)) == -1);
leftHc = find(diff(read(:,37)) == -1);
