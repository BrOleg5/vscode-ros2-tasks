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
| [`colcon: build`](.vscode/tasks.json#L12:L43)                                     | build workspace                                                  |
| [`colcon: build --packages-select`](.vscode/tasks.json#L46:L81)                   | Build only single package from workspace                         |
| [`colcon: build --clean-first`](.vscode/tasks.json#L84:L117)                      | Remove CMake cache and build workspace                           |
| [`colcon: build --packages-select --clean-first`](.vscode/tasks.json#L120:L157)   | Remove CMake cache and build only single package from workspace  |
| [`colcon: build --packages-up-to`](.vscode/tasks.json#L160:L195)                  | Build selected package including its dependencies                |
| [`colcon: build --packages-above`](.vscode/tasks.json#L198:L233)                  | Rebuild packages which depend on a specific package              |
| [`colcon: build --packages-above-and-dependencies`](.vscode/tasks.json#L236:L271) | Rebuild packages and its recursive dependencies                  |
| [`colcon: test`](.vscode/tasks.json#L276:L301)                                    | Test workspace                                                   |
| [`colcon: test --packages-select`](.vscode/tasks.json#L304:L333)                  | Test only single package from workspace                          |
| [`colcon: clean`](.vscode/tasks.json#L338:L346)                                   | Clean workspace                                                  |
| [`colcon: clean --packages-select`](.vscode/tasks.json#L349:L361)                 | Clean package workspaces                                         |
| **ROS2**                                                                          |                                                                  |
| [`ros2: Create ament_cmake package`](.vscode/tasks.json#L366:L381)                | Create a new ROS C++ package from a template                     |
| [`ros2: Create ament_python package`](.vscode/tasks.json#L384:L399)               | Create a new ROS Python package from a template                  |
| [`rqt_graph`](.vscode/tasks.json#L402:L406)                                       | Run rqt_grph tool                                                |
| **Linter**                                                                        |                                                                  |
| [`uncrustify`](.vscode/tasks.json#L413:L436)                                      | Lint files with uncrustify                                       |
| [`cpplint`](.vscode/tasks.json#L439:L451)                                         | Lint files with cpplint                                          |
| [`cppcheck`](.vscode/tasks.json#L454:L471)                                        | Run static code checker cppcheck                                 |
| [`lint_cmake`](.vscode/tasks.json#L474:L486)                                      | Run lint on cmake files                                          |
| [`flake8`](.vscode/tasks.json#L489:L501)                                          | Run flake8 on Python files                                       |
| [`pep257`](.vscode/tasks.json#L504:L516)                                          | Run pep257 on python files                                       |
| [`xmllint`](.vscode/tasks.json#L519:L531)                                         | Run xmllint on xml files                                         |
| [`lint all`](.vscode/tasks.json#L534:L545)                                        | Run all linters                                                  |

## References

1. Repository [vscode_ros2_workspace](https://github.com/athackst/vscode_ros2_workspace)
2. Repository [vscode-ros](https://github.com/ms-iot/vscode-ros)
3. YouTube playlist [Visual Studio Code ROS Extension](https://youtube.com/playlist?list=PL2dJBq8ig-vihvDVw-D5zAYOArTMIX0FA)
4. Repository [ros2_with_vscode](https://github.com/ErickKramer/ros2_with_vscode)
