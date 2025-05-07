# Productivity-Tracker-Java-
The Productivity Tracker aims to provide a simple, standalone tool for users to organize their tasks and monitor productivity. The application allows users to add, complete, and delete tasks, with progress visualized through a pie chart. It supports tracking over different time periods (daily, weekly, monthly), catering to varied planning needs. By using only the Java standard library, the project ensures accessibility and ease of deployment in any Java-supported environment.

2	Features

The application includes the following key features:
•	Task Management: Users can add tasks via a centered input form and mark them as completed using a checklist.
•	Task Deletion: A dedicated button allows users to delete selected tasks, en- hancing flexibility.
•	Time-Based Tracking: Users can switch between daily, weekly, and monthly views to filter tasks by creation date.
•	Pie Chart Visualization: A dynamic pie chart displays the proportion of com- pleted (green) versus incomplete (red) tasks.
•	Data Persistence: Tasks are saved to a text file (productivity_data.txt) with timestamps, ensuring data retention without external libraries.
•	User-Friendly GUI: Built with AWT, the interface is intuitive, with a centered input form, pie chart above it, and view selection buttons at the top.
 
3	Implementation

The project is implemented as a single Java file (ProductivityTracker.java) with the following components:

3.1	Class Structure
•	Task: Represents a task with a name, completion status, and creation timestamp (using LocalDateTime).
•	TaskManager: Manages the task list, handles text file I/O, and filters tasks by time period (daily, weekly, monthly).
•	ProductivityTrackerGUI: Implements the AWT-based GUI, including the check- list, input form, pie chart, and view selection.
•	PieChartPanel: A custom AWT panel that draws the pie chart using Graphics.
•	ProductivityTracker: The main class that initializes the application.

3.2	Technical Details
•	GUI Framework: AWT is used for lightweight, cross-platform compatibility. The layout uses BorderLayout for major regions, GridBagLayout for centering the input form and pie chart, and GridLayout for the checklist.
•	Data Storage: Tasks are stored in productivity_data.txt with the format
timestamp,taskName,completed. The java.io package handles file reading/writing.
•	Time-Based Filtering: The java.time package provides robust date handling. Tasks are filtered using LocalDate and TemporalAdjusters for weekly and monthly views.
•	Event Handling: AWT event listeners manage user interactions, such as adding tasks, marking completion, deleting tasks, and switching time periods.

