**CarND-Path-Planning-Project**

-Goal: Create a smooth path planner that can safely drive in a three-lane highway without colliding with other vehicles while also passing slower vehicles by smoothly changing lanes.

-Data on hand: the car's location Data from sensor fusion

-Initialization/Values Assumed: Speed (maximum): 50 miles per hour; actual: 49.5 miles per hour 10 m/s2 maximum acceleration Jerk (maximum speed): 10 m/s 3 4 m/s to MPH lane width 2.24 conversion factor Refresh rate of messages: 0.02s 30m grid of waypoints 0.224 is the incremental speed per step. 1 is the vehicle's preferred lane (Middle) 0 in the vehicle's left lane 2 vehicles in the right lane

-Usage: Sensor information gotten relative to our vehicle in each cycle makes a difference in producing the genuine speed and future speed of the other vehicles. Depending on these values, if our vehicle is inside 30m from the front vehicle, too_close hail is genuine. If other vehicles are too in that edge, at that point left_close or right_close hail is genuine. If our vehicle, encounters another vehicle ahead and is within the edge, at that point it changes the path to clear out or right, given they are secure and permitted; else it'll moderate down its speed. If our vehicle is moving in cleared out or right paths and there are no obstacles, it'll come back to the middle lane(preferred path). For smooth path alter or direction era (too driving inside