# Bagdeck sample bags

Sample ROS 2 bags (MCAP) for trying **Bagdeck**, a Forge app that plays back ROS 2 bags attached to Confluence pages, and answers questions about them through MCP tools. Attach one to a Confluence page and add the Bagdeck macro. The installation and test guide is linked from the app's submission.

| File | Size | What is in it |
|---|---|---|
| `robot_demo.mcap` | 6.0 MB | Synthetic, 80 s, 11 topics. A mobile robot with a camera (JPEG, 10 Hz), a depth camera, an IMU, a 6-joint arm, a laser scanner, odometry and TF, a battery and log messages. The IMU drops out for 0.4 s at 31 s on purpose. Start with this one. |
| `sensor_suite.mcap` | 4.4 MB | Synthetic, 40 s. One topic for each of the 27 `sensor_msgs` message types in ROS 2 Jazzy: images, camera info and a region of interest, IMU, magnetometer, a 3D lidar point cloud, laser scans, range, joints, GNSS with a stretch without a fix, temperature, pressure, light, humidity, battery, gamepad and feedback, and a time reference. |
| `tb3_turtlebot3_world_75s.mcap` | 5.3 MB | Recorded, 75 s. A TurtleBot3 Burger driving in the Gazebo simulator (`turtlebot3_world`), recorded with `ros2 bag record -s mcap` on ROS 2 Jazzy: camera preview, IMU, odometry, laser scan, joint states, TF and `/cmd_vel`. Header stamps are simulation time. |

The two synthetic bags come from a generator that ray-casts a small world, so every value is known exactly; they contain no real-world data. The recording was made by the author in simulation.

SHA-256:

```
22612f7f31adfb8091f7769958d7890273a39fb7960cced9b68588eb89577e8f  robot_demo.mcap
10f4d0e08a415a451d76ce12dcd3305dabfdf7cf112e53ce3a2f9e09b537f3d8  sensor_suite.mcap
55c55cff4c5f4fe757654f381bdca7ee4cf3084054cf291d2f2a47509ca9f268  tb3_turtlebot3_world_75s.mcap
```

## License

The files in this repository are dedicated to the public domain under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). TurtleBot3 and its simulation packages are by ROBOTIS (Apache License 2.0); this repository contains only a recording of their simulated output.
