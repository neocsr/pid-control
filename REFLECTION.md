# PID Controller


## Effect each of the P, I, D components

`Kp` and `Kd` are the most important parameters during the tuning.

The proportional `Kp` component controlled how fast the car will steer to minimize the cross tracking error. But that made the car jerk.
To reduce the jerking, then I tuned the derivative `Kd` component. That smoothed the steering angle and the car maneuvering was smoother. The effect of `Ki` was not that visible as it seems that the simulator doesn't have a high bias.


## Selection of Hyperparameters

I did select the parameters manually. Given a fixed value of throttle, I tuned the values of `Kp`, `Kd` and `Ki`.

`Kp` and `Kd` were the parameters that I tuned first, keeping `Ki` as zero.
Once I got the car completing a lap, I started tuning `Ki`.

I found a different set of values for each throttle value.

For example:

```
// throttle = 0.6
const double Kp = 0.06;
const double Ki = 0.0001;
const double Kd = 1.2;
```

```
// throttle = 0.5
const double Kp = 0.1;
const double Ki = 0.0;
const double Kd = 1.0;
```

```
// throttle = 0.8
const double Kp = 0.05;
const double Ki = 0.0005;
const double Kd = 1.5;
```

## Video

[Self-Driving Car - PID Controller](https://www.youtube.com/watch?v=keuRJxxd440)
