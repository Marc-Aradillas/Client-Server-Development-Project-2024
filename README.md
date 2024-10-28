# Dashboard and CRUD Module Project

## Reflection

### How do you write programs that are maintainable, readable, and adaptable?
When writing programs, I focus on clear structure and modularity to ensure that my code is maintainable, readable, and adaptable. For example, in Project One, I developed a CRUD Python module that adhered to the principles of encapsulation by separating database operations into distinct functions such as `create`, `read`, `update`, and `delete`. This modular approach made it easier to debug and extend the functionality, allowing for the same module to be reused in Project Two to connect the dashboard widgets to the database.

The advantages of working this way include easier maintenance, as code changes or improvements can be localized within a module without affecting other components. It also facilitates readability for future developers who may work on the codebase, as each function is designed to perform a single, well-defined task. The CRUD module could be repurposed in future projects to interact with other databases, whether for administrative dashboards, data processing, or even integrating with web services.

### How do you approach a problem as a computer scientist?
I approach problems systematically, breaking them down into smaller, manageable components. For the Grazioso Salvare dashboard project, I started by understanding the requirements for the database queries and dashboard components. I first implemented the database connection using the CRUD module, then moved on to building the interactive dashboard with filtering options. This approach ensured that each step was functional before proceeding to the next phase.

Compared to previous assignments, this project required more complex data manipulation, so I used aggregation pipelines and data visualization techniques to meet the requirements. In the future, I would continue to use a modular approach to design databases and user interfaces, integrating testing early on to verify that each component meets the client's needs. I would also employ version control to track changes and collaborate more effectively with other developers.

### What do computer scientists do, and why does it matter?
Computer scientists solve real-world problems by developing software solutions that improve efficiency and effectiveness. In the context of this project, I developed a dashboard for Grazioso Salvare, allowing them to better manage and visualize their animal data. By providing filtering options and a geolocation map, I made it easier for the company to identify suitable rescue animals based on specific criteria, ultimately helping them streamline their operations.

The work of computer scientists matters because it enables organizations to leverage data for informed decision-making, automate tedious tasks, and improve the user experience for customers. In this project, my contributions helped Grazioso Salvare to manage animal data more effectively, which could lead to better outcomes in their rescue operations.

## Submission
This repository contains the final dashboard code and the README file from Project Two.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Project Overview
This project demonstrates the development of a MongoDB-connected dashboard for the Grazioso Salvare rescue animal organization, leveraging data filtering and visualization tools for database interactions. The application is built using Dash, Plotly, and MongoDB, and allows the client to dynamically filter animals based on different rescue categories (Water Rescue, Mountain/Wilderness Rescue, Disaster/Individual Tracking), as well as visualize animal breeds through interactive charts and maps.

## Project Functionality
The dashboard provides the following key functionalities:
- **Data Filters:** The user can select from various rescue types to filter the displayed animals.
- **Interactive Data Table:** The table dynamically updates based on the selected rescue type, displaying data such as breed, location, age, and outcome.
- **Pie Chart Visualization:** A pie chart visualizes the percentage breakdown of different dog breeds based on the filter.
- **Geolocation Mapping:** A map updates to show the location of a selected dog from the table.

The dashboard allows users to select rows from the data table to display the corresponding geolocation on the map and view the selected dog’s breed distribution in the pie chart.

## Tools Used
### MongoDB
MongoDB is used to store the animal data and provide real-time access via the CRUD Python module. MongoDB is ideal for this project due to its flexible document-based storage, making it easier to work with varied and semi-structured animal data.

### Dash & Plotly
Dash is used to create the interactive web application. Plotly, integrated within Dash, enables dynamic charting capabilities, such as the pie chart representing dog breeds. Dash provides an efficient way to manage callbacks that update the data table, pie chart, and map based on user interactions.

## How to Reproduce the Project
1. **MongoDB Setup:** Ensure MongoDB is running and populated with the Austin Animal Center Outcomes dataset. Use the provided `AnimalShelter` CRUD class to interact with MongoDB.
2. **Install Required Libraries:** Install the necessary Python libraries:
   ```bash
   pip install dash jupyter-dash dash-leaflet pymongo pandas plotly
3. Run the Dashboard: Start the dashboard by running the Jupyter notebook or Python file where the dashboard code resides.
4. **Interact:** Use the filter buttons and click on table rows to view the corresponding pie chart and geolocation

## Screenshots
Below are the screenshots of the dashboard functionality:

- **Dashboard Initial State:** The dashboard loads with the data table and filter options, but without any specific filtering applied.

![image](https://github.com/user-attachments/assets/d8216286-ee3b-4e58-bdeb-1bd7cd15820f)


![image](https://github.com/user-attachments/assets/10bc0ee6-74ec-4fa5-9fd4-07370e4e3fae)


- **Water Rescue Filter:** This screenshot shows the dashboard after selecting the "Water Rescue" filter. The table updates to show only animals suited for water rescue, and the pie chart visualizes the breed distribution of these animals. Labrador Retrievers dominate the pie chart when "Water Rescue" is selected, indicating their prevalence in this rescue type.

![image](https://github.com/user-attachments/assets/17119528-bac0-4103-bba4-6c2ed1e19480)


- **Mountain/Wilderness Rescue Filter:** After selecting "Mountain/Wilderness Rescue", the table displays relevant animals, and the pie chart updates accordingly.

![image](https://github.com/user-attachments/assets/ec2e1ea5-b924-4305-98de-6bca3c6351d0)


- **Disaster/Individual Tracking Filter:** This screenshot shows the data filtered for Disaster or Individual Tracking rescue types.

![image](https://github.com/user-attachments/assets/f480aa56-5998-4fe1-af4e-11bcb7cafa37)


- **Reset Filter:** The dashboard in its reset state, displaying the unfiltered data.

![image](https://github.com/user-attachments/assets/6d8b428c-e012-4a15-b45f-a1323837257c)

   
## Challenges Encountered
During development, the following challenges were addressed:

- **Data Filtering**: Implementing dynamic filters based on rescue types required understanding MongoDB query structures and integrating them into Dash callbacks.
- **Visualization:** Customizing the pie chart layout to accommodate the breed labels without overlapping required adjusting the textinfo and textposition attributes.
- **Callback Debugging:** Ensuring that all callbacks, especially for the map and pie chart, were correctly updating based on user interaction.
These challenges were resolved through careful debugging, refining the query logic, and leveraging Dash’s callback functions.

## Resources
- **MongoDB Documentation:** MongoDB official documentation for details on database setup, queries, and Python integration.
- **Dash Documentation:** Official Dash documentation, essential for building interactive charts and dashboards.
- **Plotly Documentation:** Provides information on creating interactive plots using Plotly.
- **Austin Animal Center Outcomes Dataset:** Grazioso Salvare's dataset for rescue animals, which forms the basis of this project’s MongoDB database.
- **Python Dash Walkthrough:** The Dash walkthrough from Module 6 was instrumental in understanding how to implement callbacks and dashboard components effectively.

## Conclusion
This project successfully meets the client’s requirements by allowing Grazioso Salvare to interactively filter, view, and map animals from the Austin Animal Center Outcomes dataset. The use of MongoDB for real-time data access, coupled with Dash for dynamic visualization, makes the application both functional and visually informative.
