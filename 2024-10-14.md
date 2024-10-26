# Summary
1. learned [_InGVIO: A Consistent Invariant Filter for Fast and High-Accuracy GNSS-Visual-Inertial Odometry_](https://ieeexplore.ieee.org/document/10040716) and achieved the results of the experiments.
   Since it includes GNSS, the VIO part simplifies the visual update with a new marginalization strategy. It may cause a decrease in accuracy, but makes visual fusion faster.
2. learned [_MSCEqF: A Multi State Constraint Equivariant Filter for Vision-Aided Inertial Navigation_](https://ieeexplore.ieee.org/document/10325586) and haven't really understood, the code didn't work well.
   It can be directly applied to the actual scenario with only a small amount of tuning and no additional checks.
3. learned [_Enhancing VIO Robustness Under Sudden Lighting Variation: A Learning-Based IMU Dead-Reckoning for UAV Localization_](https://ieeexplore.ieee.org/document/10473050/) and haven't had the ability to reproduce the results.
   It is a dead reckoning algorithm that relies solely on inertial measurements(LIDR)  which  is used to solve the problem of deterioration of VIO performance caused by sudden changes in light. By the way, this paper also brings LIDR and VIO together. When the light is good, it is estimated with VIO. Otherwise, LIDR is used.
4. learned [_A Combined Visual-Inertial Navigation System of MSCKF And EKF-SLAM_](https://ieeexplore.ieee.org/document/9018998).
   It talks a little about the difference between MSCKF and EKF-SLAM and brings them together.
# Plan 
1. read a paper about VIO or VI-SLAM in early years to learn about some basic knowledge
2. read a paper about VIO or VI-SLAM in recent years and organize the content
3. listen to the courses about SLAM-14
# Problem
1. Why GNSS combined with VI enables smooth attitude estimation drift-free?
   Becasue GNSS  can obtain global information from satellites to calculate the absolute position and then an external reference is provided which can eliminate the accumulated error of the VI system.
2. What is the issue of consistency that filtering-based approaches need to deal with?
   The consistency is to require the algorithm being consistent and stable in the processing results of the input data. The algorithm is required to be able to continuously provide accurate and stable pose and map information during operation in the VIO system. Influencing factors include the algorithm itself, parameter settings,  multi-sensor fusion and so on.
3. Marginalization Strategy and Anchor Change
   Haven't understood clearly.
4. Lie Groups and Symmetries
   Lie Groups has already learned, but Symmetries is hard to understand for me right now.