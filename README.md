# GoFa Palettizer Useful Code Snippets Repository 🤖

This repository contains useful code snippets for the GoFa CRB15000 Palettizer. The code is written in RAPID, a high-level language used for programming ABB industrial robots.

## Kinematics 🦕

An Excel file reports the kinematic parameters of the GoFa CRB15000 variants. The file contains the Denavit-Hartenberg parameters, see GoFa™: Kinematic and dynamic parameters
of GoFa 5 TechNote.

## Custom MoveL and MoveJ Functions 🤖

The `MoveLHomeMade` and `MoveJHomeMade` functions are custom movement functions designed to move the robot to a specific position while avoiding singularities. These functions ensure that joint 4 is always at 0° and joint 5 is always at 90°. 

### Requirements 

The tool has to have the tool0 orientation and only with z-value. Workobjects and targets have to be reachable by the robot in palletizing configuration.

### Usage 

You can use these functions in the same way as the standard `MoveL` and `MoveJ` functions in RAPID:

```RAPID
    ! Like MoveL and MoveJ
    MoveJHomeMade Target_10, v1000, fine, MyTool\WObj:=wobj0;
    MoveLHomeMade Target_20, v1000, fine, MyTool\WObj:=wobj0;
```

## Contributing 🚀
We welcome contributions to improve this code. If you encounter any issues or have suggestions for improvements, please report them. Feel free to fork this repository and submit pull requests with your proposed changes.

## License 📝
This project is licensed under the MIT License. Please see the LICENSE file for more details.