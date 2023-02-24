# Visual Studio Code ROS2 Tasks

Tasks for ROS2 workflow in Visual Studio Code (Windows, Linux).

## Requirements

Obviously required:

- [VSCode](https://code.visualstudio.com)
- [ROS2](https://www.ros.org)
- [colcon](https://colcon.readthedocs.io/en/released/)
- [xmllint](https://gitlab.gnome.org/GNOME/libxml2)

VSCode extensions:

- ROS ([VS Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-iot.vscode-ros), [Github](https://github.com/ms-iot/vscode-ros))
- ROS2 Ament Task Provider ([cite](https://www.althack.dev/vscode-ament-task-provider/v0.2.0/), [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=althack.ament-task-provider), [Github](https://github.com/athackst/vscode-ament-task-provider))
- Tasks Shell Input ([VS Marketplace](https://marketplace.visualstudio.com/items?itemName=augustocdias.tasks-shell-input), [Github](https://github.com/augustocdias/vscode-shell-command))
- multi-command ([VS Marketplace](https://marketplace.visualstudio.com/items?itemName=ryuta46.multi-command), [Github](https://github.com/ryuta46/vscode-multi-command))

Colcon extensions:

- [colcon-clean](https://github.com/colcon/colcon-clean)

## Tasks

| Task (clickable)                                                                  | Description                                                      |
|:----------------------------------------------------------------------------------|:-----------------------------------------------------------------|
| **Colcon**                                                                        |                                                                  |
| [`colcon: build`](.vscode/tasks.json#L12:L44)                                     | Build workspace                                                  |
| [`colcon: build --packages-select`](.vscode/tasks.json#L47:L83)                   | Build only single package from workspace                         |
| [`colcon: build --clean-first`](.vscode/tasks.json#L86:L120)                      | Remove CMake cache and build workspace                           |
| [`colcon: build --packages-select --clean-first`](.vscode/tasks.json#L123:L161)   | Remove CMake cache and build only single package from workspace  |
| [`colcon: build --packages-up-to`](.vscode/tasks.json#L164:L200)                  | Build selected package including its dependencies                |
| [`colcon: build --packages-above`](.vscode/tasks.json#L203:L239)                  | Rebuild packages which depend on a specific package              |
| [`colcon: build --packages-above-and-dependencies`](.vscode/tasks.json#L242:L278) | Rebuild packages and its recursive dependencies                  |
| [`colcon: test`](.vscode/tasks.json#L283:L309)                                    | Test workspace                                                   |
| [`colcon: test --packages-select`](.vscode/tasks.json#L312:L342)                  | Test only single package from workspace                          |
| [`colcon: clean`](.vscode/tasks.json#L347:L355)                                   | Clean workspace                                                  |
| [`colcon: clean --packages-select`](.vscode/tasks.json#L358:L368)                 | Clean package workspaces                                         |
| **ROS2**                                                                          |                                                                  |
| [`ros2: Create ament_cmake package`](.vscode/tasks.json#L375:L390)                | Create a new ROS C++ package from a template                     |
| [`ros2: Create ament_python package`](.vscode/tasks.json#L393:L408)               | Create a new ROS Python package from a template                  |
| [`rqt_graph`](.vscode/tasks.json#L411:L415)                                       | Run rqt_grph tool                                                |
| **Linter**                                                                        |                                                                  |
| [`uncrustify`](.vscode/tasks.json#L422:L445)                                      | Lint files with uncrustify                                       |
| [`cpplint`](.vscode/tasks.json#L448:L460)                                         | Lint files with cpplint                                          |
| [`cppcheck`](.vscode/tasks.json#L463:L480)                                        | Run static code checker cppcheck                                 |
| [`lint_cmake`](.vscode/tasks.json#L483:L495)                                      | Run lint on cmake files                                          |
| [`flake8`](.vscode/tasks.json#L498:L510)                                          | Run flake8 on Python files                                       |
| [`pep257`](.vscode/tasks.json#L513:L525)                                          | Run pep257 on python files                                       |
| [`xmllint`](.vscode/tasks.json#L528:L540)                                         | Run xmllint on xml files                                         |
| [`lint all`](.vscode/tasks.json#L543:L554)                                        | Run all linters                                                  |

## Usage

Build tasks run with command "Tasks: Run Build Task" (default hotkey `Ctrl+Shift+B`).
All tasks (include build) run with command "Tasks: Run Tasks" (default hotkey is not defined). You may set convenient hotkey, e.g. `Alt+T`.

## References

1. Repository [vscode_ros2_workspace](https://github.com/athackst/vscode_ros2_workspace)
2. Repository [vscode-ros](https://github.com/ms-iot/vscode-ros)
3. YouTube playlist [Visual Studio Code ROS Extension](https://youtube.com/playlist?list=PL2dJBq8ig-vihvDVw-D5zAYOArTMIX0FA)
4. Repository [ros2_with_vscode](https://github.com/ErickKramer/ros2_with_vscode)
