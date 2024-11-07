# CoursePlanner

CoursePlanner is a C++ project designed to simplify and manage the complex process of planning courses, including managing prerequisites and determining the most optimal course schedule for students. This project is particularly useful for students dealing with complicated prerequisite structures, like those at Purdue University, ensuring that graduation requirements are met efficiently within a defined timeframe.

## Features

1. **Prerequisite Management**: Stores all prerequisite information for each course, including credits and mandatory or elective status.
2. **Course Availability**: Identifies which courses are available based on completed prerequisites, including support for concurrent courses.
3. **Course Importance Ranking**: Determines the importance of each course based on how many other courses require it, both horizontally (number of dependent courses) and vertically (depth of prerequisites).
4. **Graduation Feasibility Check**: Calculates whether a given plan can meet graduation requirements within a specified number of semesters.
5. **Credit Limits**: Issues warnings if the planned number of credits for a semester exceeds the limit (e.g., 20 credits).

## Project Structure

The project is organized into multiple files, each serving a specific purpose:

- **main.cpp**: The main entry point of the program, handling user input and orchestrating course planning.
- **coursePrerequisite.cpp**: Manages the dictionary that stores course prerequisite information, including credits and prerequisites.
- **planCourses.cpp**: Contains the core logic for finding available courses, ranking course importance, and validating course plans for each semester.
- **utils.cpp**: Contains utility functions that support main program logic.

## Usage

1. Clone the repository to your local machine.
   ```sh
   git clone https://github.com/yourusername/CoursePlanner.git
   ```
2. Compile the project using a C++ compiler, such as g++.
   ```sh
   g++ main.cpp coursePrerequisite.cpp planCourses.cpp utils.cpp -o CoursePlanner
   ```
3. Run the executable to start planning your course schedule.
   ```sh
   ./CoursePlanner
   ```

## Example

The following example demonstrates how to define courses and plan the semesters:

- **Courses**: Course "A" requires "B" as a prerequisite, and course "B" has no prerequisites. Each course is assigned a credit value, and certain courses are marked as mandatory.
- **Semester Plan**: The user can input planned courses for each semester, and the program will validate if the plan is feasible.

If the plan is infeasible due to unmet prerequisites, credit overload, or uncompleted mandatory courses, the program will issue warnings and suggestions.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request if you have any improvements or features you'd like to add.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

