## Section 5.4.4: CBF tuning for Leader-Follower
Th objective for the follower is to keep leader inside the field-of-view and, preferably, at the center. Adaptation is needed as depending on the pattern of leader's movement, different policy parameters perform better. The policy here is a CBF-CLF-QP that is to be satisfied in expectation when dynamics is uncertain. The first sim shows the performance of default parameters. The second one shows improvemwnt with our adaptation running online. Results change significantly when control input bounds are imposed. The QP does not even exhibit a solution after some time when default parameters are used and the simulation ends. The proposed algorithm is able toadapt parameters online to continuously satisfy input bounds. The prediction horizon is taken to be 20 time steps.

|  | No Adaptation | With adaptation |
| --------------| -------------------| -----------------|
| No input bound | ![no_adapt_no_bound](https://user-images.githubusercontent.com/19849515/192348004-6dcbf70f-2db5-49dd-9f4f-04370dc028e4.gif) | ![adapt_no_bound](https://user-images.githubusercontent.com/19849515/192348165-5f6fbaf4-81e1-4cd6-893f-d5f763ea9cbc.gif) |
| With input bounds | ![no_adapt_with_bound](https://user-images.githubusercontent.com/19849515/192348231-a921fa36-6198-45b5-94c2-80ae87ab8b39.gif) | ![adapt_with_bound](https://user-images.githubusercontent.com/19849515/192348335-448600b8-042b-4bb5-8c9f-17e654584336.gif)

## Section 5.4.6.2: Quadrotor Experiments

Default parameters: 
https://youtu.be/G3gOAOpJPXM

[![IMAGE ALT TEXT HERE]((https://github.com/user-attachments/assets/29f48cce-bebc-4393-9924-95cc655f5ede))](https://youtu.be/G3gOAOpJPXM)





 Proposed: 
https://youtu.be/ibTU8vpVa34

{% include youtube.html id="ibTU8vpVa34" %}

## Section 5.5: Risk-aware MPPI for Stochastic Hybrid Systems

[Python and gazebo simulations](https://youtu.be/0JyLC5gSw8g)

https://github.com/user-attachments/assets/c75edbed-d587-4282-b8d9-2c74940301af


![Screenshot from 2024-11-01 12-28-36](https://github.com/user-attachments/assets/29f48cce-bebc-4393-9924-95cc655f5ede)
