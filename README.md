# Course Registration Simulation
This project simulates a course registration system for 100 students, where each student has preferences for courses they would like to take. The simulation includes clustering students based on their course preferences and attempts to assign them to available course sections. It also checks for overbooked courses. The project uses K-means clustering for grouping students and a simple algorithm to assign students to their preferred courses based on availability.

## Project Components
1. Data Generation
- Students: A list of 100 students, each with a unique ID and a list of 3 course preferences (out of 4 available courses: Math, CS, Physics, and Biology). The preferences are randomly assigned.
- Courses: A set of courses with sections and capacity limits:
    - Math: 2 sections, 30 seats each
    - CS: 2 sections, 30 seats each
    - Physics: 1 section, 20 seats
    - Biology: 1 section, 20 seats

2. Student Clustering:
- K-means clustering is used to group students into 3 clusters based on their course preferences.
The idea is that students with similar preferences are grouped together, allowing for better understanding of student behavior in course selection.

3. Course Assignment:
- The system attempts to assign students to their course preferences in order of priority, while considering the capacity limits of each course section.
If a student’s top course choice is full, they are assigned to their next available preference, and so on.

4. Overbooked Courses Check:
- After students are assigned to courses, the system checks if any course has more students assigned than its capacity. If a course is overbooked, the number of students exceeding the course's capacity is reported.

## Installation
To run this project locally, make sure you have the following dependencies installed:

``bash
pip install numpy scikit-learn

## Usage 
1. Run the simulation:
- Clone or download this repository.
- Open the project folder in a Python environment (e.g., Jupyter Notebook, Python script, or VSCode).
- Execute the code to simulate the course registration process and check for overbooked courses.
``bash
python course_registration_simulation.py

2. Modify the configuration:

You can modify the number of students, the list of available courses, or the course capacity to simulate different scenarios.

3. Outputs:

The program will output the list of overbooked courses (if any) after all students are assigned to their courses.
Example output: { "Physics": 5, "Biology": 3 }, indicating that Physics and Biology courses are overbooked.

## Future Improvements
- Advanced Course Assignment Algorithms: Instead of simply assigning students to courses based on availability, more sophisticated algorithms (like those used in real-life registration systems) can be used to handle course preferences better.
- User Interface: Adding a GUI or web interface for users to modify student preferences, course capacities, and see real-time registration statuses.
- Visualization: Visualize the clustering results and course assignments using plots to better understand student behavior.

## Acknowledgments
The project uses the scikit-learn library for clustering.
Thanks to the creators of numpy for their efficient array operations.
