---
{"dg-publish":true,"permalink":"/Knowledge/School/B-Intro to Autonomous Mobile Robots/","title":"Introduction to Autonomous Mobile Robots","tags":["book/textbook/MTRE"]}
---



# 3 Mobile Robot Kinematics

## 3.1 Introduction
- Kinematics- the study of how mechanical systems behave
	- manipulator robots are much more complex but extensively studied 
		- made simple by having one side of the arm in a fixed location relative to the environment
	- mobile robots are harder to calculate kinematics due to the challenge of position estimation
		- not being able to absolutely calculate the location of the end effector through sensor data

## 3.2 Kinematic Models and Constraints
- Deriving a model for the whole robot is a bottom up process
	- forces and constraints of each wheel contribute to the robot's motion
		- connection to the chassis constrain the overall motion of the Robot
	- **all forces on the robot must be expressed with respect to a clear and consistent reference frame**

- Robot Chassis only refers to the rigid body of the robot
	- ignoring the joints and degrees of freedom internal to the robot and its wheels

- Local reference frame of the robot: $P:{X_{R},Y_{R}}$ 
	- P is point on the robot chassis chosen as the position reference point
- Global Reference frame: $O:X_{I},Y_{I}$ 
	- Position of P is denotated by x and y with the angular difference between global and local given by $\Theta$ 
	-  $\xi_{I}=\begin{bmatrix}x\\y\\\theta\end{bmatrix}$ 
- to map the motion along the axes of the global reference frame to motion along the axes of the local reference frame use the *orthogonal rotation matrix* below
	-  $R(\theta)=\begin{bmatrix} \cos\theta & \sin \theta & 0 \\ -\sin \theta & \cos \theta & 0 \\ 0&0&1 \end{bmatrix}$ 

### Kinematic Variables

|                               Name                                |       Symbol        |
|:-----------------------------------------------------------------:|:-------------------:|
|                          wheel diameter                           |       $r_{n}$       |
|                       Robot Reference Point                       |         $P$         |
|               Polar Position of wheel relative to P               |   $A=(l,\alpha)$    |
|                            Wheel Speed                            | $\dot{\varphi_{n}}$ |
|                  wheel plane relative to chassis                  |       $\beta$       |
|                     steering angle over time                      |     $\beta(t)$      |
|                       wheel spin over time                        |    $\varphi(t)$     |
| Swedish: angle b/w main wheel plane & axis of rotation of rollers |      $\gamma$       |

|                                                                   |                     |


## Wheel Kinematic Constraints

|                  Figures                  |            Wheel Type             |                                                        Rolling Constraint                                                        |                                                                   Sliding Constraint                                                                   |
|:-----------------------------------------:|:---------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------:|
| ![[Pasted image 20220118021954.png\|200]] |          Fixed Standard           |                   $\begin{bmatrix}\sin(\alpha+\beta)&-\cos(\alpha+\beta)&(-l)\cos \beta\end{bmatrix}R(\theta)\dot{\xi_I}-r\dot{\varphi}=0$                   |                                      $\begin{bmatrix}\cos(\alpha+\beta)&\sin(\alpha+\beta)&l\sin \beta\end{bmatrix}R(\theta) \dot{\xi_{I}}=0$                                      | 
|   ![[Pasted image 20220118022151.png\|200]]    | Steered Standard $\beta=\beta(t)$ |                   $\begin{bmatrix}\sin(\alpha+\beta)&-\cos(\alpha+\beta)&(-l)\cos \beta\end{bmatrix}R(\theta)\dot{\xi_I}-r\dot{\varphi}=0$                   |                                      $\begin{bmatrix}\cos(\alpha+\beta)&\sin(\alpha+\beta)&l\sin \beta\end{bmatrix}R(\theta) \dot{\xi_{I}}=0$                                      | 
|   ![[Pasted image 20220118022740.png\|200]]    |              Castor               |                   $\begin{bmatrix}\sin(\alpha+\beta)&-\cos(\alpha+\beta)&(-l)\cos \beta\end{bmatrix}R(\theta)\dot{\xi_I}-r\dot{\varphi}=0$                   |                              $\begin{bmatrix}\cos(\alpha+\beta)&\sin(\alpha+\beta)d&l\sin \beta\end{bmatrix}R(\theta)\dot{\xi_{I}}+d \dot{\beta}=0$                               | 
|   ![[Pasted image 20220118022824.png\|200]]    |              Swedish              | $\begin{bmatrix}\sin(\alpha+\beta+\gamma)&-\cos(\alpha+\beta+\gamma)&(-l)\cos(\beta+\gamma)\end{bmatrix}R(\theta)\dot{\xi_{I}}-r \dot{\varphi}\cos \gamma=0$ | $\begin{bmatrix}\cos(\alpha+\beta+\gamma)&\sin(\alpha+\beta+\gamma)&l\sin(\beta+\gamma)\end{bmatrix}R(\theta) \dot{\xi_{I}}-r \dot{\varphi}\sin \gamma-r_{sw}\dot{\varphi_{sw}}=0$ |
|   ![[Pasted image 20220118022859.png\|200]]    |             Spherical             |                 $\begin{bmatrix}\sin(\alpha+\beta)&-\cos(\alpha+\beta)&(-l)\cos \beta\end{bmatrix}R(\theta)\dot{\xi_{I}}-r \dot{\varphi}=0$                  | $\begin{bmatrix}\cos(\alpha+\beta)&\sin(\alpha+\beta)&l\sin \beta\end{bmatrix}R(\theta)\dot{\xi_{I}}=0$                                                                                                                                                        |


## Robot kinematic Constraints
|                   Description                   |     Variable     |
|:-----------------------------------------------:|:----------------:|
|          # of fixed wheels on a Robot           |     $N_{f}$      |
|         # of steered wheels on a Robot          |     $N_{s}$      |
|       variable steering angle of $N_{s}$        |  $\beta_{s}(t)$  |
|             orientation of $N_{f}$              |   $\beta_{f}$    |
|                   Fixed cases                   | $\varphi_{f}(t)$ |
|                  Steered cases                  | $\varphi_{s}(t)$ |
|         matrix of Fixed & Steered cases         |   $\varphi(t)\begin{bmatrix}\varphi_{f}(t) \\ \varphi_{s}(t)\end{bmatrix}$   |
| constant diagonal NxN matrix of all wheel radii |     $J_{2}$      |
|                                                 |                  |

- Rolling constraints of all wheels can be collected in this equation
	-  $J_{1}(\beta_{s})R(\theta)\dot{\xi_{I}}-J_{2}\dot{\varphi}=0$  

- Matrix with projections for all wheels to their motions along their individual wheel plane
	-  $J_{1}(\beta_{s})\begin{bmatrix}J_{1f} \\ J_{1s(\beta_{s})} \end{bmatrix}$ 



## Mobile Robot Maneuverability

