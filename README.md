There are two files in this repository: collisionraw.txt  and collisionprocessed.csv

File name: collisionraw.txt
This file contains the raw data issued from LAMMPS using a special extension that tracks and records collision information. The control plane is placed at the z coordinate 22.3. The columns are the information of an atom when it crosses the control plane:
He atom number, time step, coordinate x, coordinate y, coordinate z, velocity Vx,  velocity Vy, velocity Vz, penetration depth Dz, displacement Dx, Displacement Dy
At the start of the collision, vz is negative and the variables Dx, Dy, Dz are set = 0.
At the end of the collision, vz is positive and the variables Dx, Dy, Dz are non zero.

File name: collisionprocessed.txt
This file is obtained by post processing the file collisionraw.txt, puting all the information of each collision event together. There are 13 columns in the data
1: Index of the collision, 2: atom Id (from 1 to 40), 3: the beginning time of the collision Timein, 4: incoming velocity Vx, 5: incoming velocity Vy, 6: incoming velocity Vz
7: the ending time of the collision Timeout, 8: outgoing velocity Vx, 9: outgoing velocity Vy, 10: outgoing velocity Vz, 11: the surface displacement along x, 
12: the surface displacement along y, 13: the residence time (= column 7 - column 3)
