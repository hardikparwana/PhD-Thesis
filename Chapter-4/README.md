
## Simulation Results

## Section 4.3.3.3

Here is an example simulation run:

The ego agent (red) navigates to its goal location while performing collision avoidance with other agents (black).


- Standard method

  The CBF-QP becomes infeasible although the robot is still safe

https://github.com/user-attachments/assets/443b6936-1815-4ceb-9f42-ab2937eb3497


- Proposed method

  The proposed method is able to adapt the parameters and maintain feasibility of controller at all times

https://github.com/user-attachments/assets/63b85d00-6dfd-4e19-a76f-667b19e24715


## Section 4.3.4 Trust based Adaptation

Unicycles and double integrator ego agents navigate in presence of single integrator modeled adversaries and uncooperative agents in 2D and 3D.

### Scenario 1(2D):
| Constant CBF parameter | Trust based adaptation |
| --------------| -------------------|
| ![no_adapt](https://user-images.githubusercontent.com/19849515/227721767-75d395db-ca03-47b3-a1cd-08284ad61e6d.gif)| ![trust_adapt](https://user-images.githubusercontent.com/19849515/227721791-3695f2fa-b748-4309-92fa-3d8fb2dfe6f3.gif) |

### Scenario 2(3D): 
| Constant CBF parameter | Trust based adaptation |
| --------------| -------------------|
| ![trust_fixed_parameter](https://user-images.githubusercontent.com/19849515/227721066-e2492b6c-eb11-4a0a-86df-677381d555c3.gif) | ![trust_adaptive](https://user-images.githubusercontent.com/19849515/227721079-a36a6ab0-cb4d-4f57-84d8-bf4628020085.gif) |

## Section 4.4.7.3 Predictive framework for Leader-Follower problem
The follower's objective is to keep leader inside the field of view(FoV) while maximizing the reward which is maximum when leader is at the center of FoV. The leader moves independently and therefore visibility maintainence is a time-varying constraint for the follower. Our proposed method is able to adapt the parameters for better performance. 

When no input bounds are imposed, the proposed method is able to maintain the leader at center of FoV better than fixed parameter case. When input bounds are present, the default CBF parameters fail to ensure a solution of QP controller soon after the simulation starts. The proposed method on the other hand is able to quickly adapt parameters to maintain FoV constraint while still satisfying input bounds. Due to limited actuation, the algorithm learns that it is not feasible to focus on performance and minimzes turning motion to ensure that leader remains inside FoV (if the follower were to turn too much, it wouldn't be able to turn back on time due to limited actuation).

|  | No Adaptation | With adaptation |
| --------------| -------------------| -----------------|
| No input bound | ![no_bound_no_adapt](https://user-images.githubusercontent.com/19849515/227720687-a3f1142f-7004-4c7d-b572-b90d29fb6d71.gif) | ![adapt_no_bound](https://user-images.githubusercontent.com/19849515/227720750-57c96b16-f799-44ae-b97d-8fe5f21349dc.gif) |
| Input Bound | ![no_adapt_with_bound](https://user-images.githubusercontent.com/19849515/227720777-b5909dec-079d-4dc3-8562-d94a4118f344.gif) | ![adapt_with_bound](https://user-images.githubusercontent.com/19849515/227720799-cfb15944-8b8e-425c-82a5-33349336f1b3.gif) |




