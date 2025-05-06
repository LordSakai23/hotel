# Hotel Management
This is a code that displays the available rooms and the times its available in a hotel and also displays the restaurant menus to the user while giving them the ability to book free rooms.

## System Requirements

- Main Menu options 
- Personal details: including type of room and service booked. 
- Hotel room details: Type of room, number of persons, number of beds, what is included in the room i.e. on-suite, couch, TV etc. 
- Bookings 
- Billing and payments 
- Record keeping guest records, guests and allocated rooms, vacancy of rooms, room services 
- Database CSV document for customer / guests’ details 
- Test table to show that the system works. 
## Client Requirement 
 
| Requirement ID    | Description   | Mandatory [M] or desirable [D] |
| ------------- | ------------- | ------------- |
| 1  | log into system  | D |
| 2  | creating Booking   | M |
| 3  | Room details  | M |


Target Users

Understanding the application's end users is crucial for tailoring feedback, usability improvements, and technical refinement. The target users are grouped into two broad categories: technical and non-technical, to ensure well-rounded feedback that covers both functionality and user experience.

Technical Users

These individuals have a programming background or relevant technical experience, which qualifies them to provide insight on code quality, structure, logic, and integration mechanisms. They include:

1. Friends with programming experience: Peers who can offer casual but insightful reviews based on their familiarity with best coding practices.
2. Co-workers from work experience placements: Professionals who have worked in real-world environments and understand production-grade code, database connectivity, and scalable architecture.
3. Tutors or lecturers from college: Academics or instructors who are familiar with theoretical foundations and can provide structured critiques or advice on improving design, structure, and maintainability.

Non-Technical Users

These individuals represent the typical end-user who may use the application but lacks a technical background. Their feedback is critical for refining the user experience, interface design, and accessibility. They include:

1. Friends without a technical background: Everyday users who can test the app’s intuitiveness, navigability, and visual appeal.
2. Family members: A diverse group with various levels of digital literacy who can highlight ease-of-use issues.
3. Colleagues in non-technical roles: Office workers or users who can assess how practical the application is for people who rely on software but don’t build it.

Feedback Gathering Methods
A combination of qualitative and quantitative methods will be used to gather comprehensive feedback. The two main methods selected are Focus Groups and Surveys.

1. Focus Groups
Focus groups are small, moderated discussions involving selected users. These sessions are designed to provide qualitative, in-depth feedback through open conversation and observation.

Technical Focus Group

This group will consist of technically skilled individuals with hands-on experience in programming languages like C# and SQL databases. The primary goal is to analyse the core functionality of the application from a software development perspective. Topics to cover include:

1. Reviewing the structure, logic, and efficiency of the code
2. Identifying bugs, inconsistencies, or inefficiencies
3. Recommending improvements for database interactions, class usage, or code modularity
4. Discussing whether the system design supports scalability and maintainability

Non-Technical Focus Group

This group is composed of users without a development background who will interact with the application as end users. This discussion will focus on:

1. Evaluating the visual design, such as the colour scheme and layout
2. Testing navigational flow to assess how easy it is to move between sections
3. Highlighting elements that might be confusing or overwhelming
4. Suggesting improvements to enhance intuitiveness and user satisfaction

2. Surveys
Surveys will be used to collect structured, measurable feedback from a broader group of users. They provide data that can be quantified to track trends and assess the effectiveness of different features. Surveys will be customized to gather insights based on the technical level of the respondent.

Technical survey responses will help evaluate backend efficiency, programming practices, and code structure.
Non-technical survey responses will gauge user satisfaction, visual appeal, accessibility, and engagement.

Surveys will be conducted using online tools and distributed across different platforms such as email, social media, and internal channels.

Expected Feedback
Anticipating the types of feedback in advance helps prepare for actionable analysis. Feedback will fall into both positive and negative categories.

Negative Feedback

1. Comments about poorly structured or unorganized code
2. Feedback highlighting a lack of proper code commenting and documentation
3. Issues related to performance, bugs, or difficulties with database connectivity
4. Complexity in interface design that might confuse non-technical users

Positive Feedback

1. Praise for a clean, visually appealing, and coherent user interface
2. Appreciation of ease of use, simple navigation, and clear functionality
3. Encouragement related to the innovative nature of the project or its usefulness
4. Positive recognition of the environmental theme and purpose of the application

This feedback will be compiled, analysed, and used to inform further iterations and improvements of the application.

Focus Group Questions
Two sets of questions will be presented to the respective groups during focus group sessions. These will guide the discussion and ensure that all relevant areas are covered.

Technical Questions

1. Is the code well-commented and easy to follow?
2. Are the variable names descriptive and appropriate?
3. What’s the best approach to linking this code to the database?
4. Are the carbon footprint calculations accurate and efficient?

These questions aim to probe deeper into the **software engineering quality** of the application—maintainability, logic, performance, and database integrity.

Non-Technical Questions

1. Is the colour scheme visually appealing and appropriate?
2. Does the user interface feel intuitive and easy to use?
3. Is it easy to navigate through the application?
4. Does the overall application look too complex for everyday users?

These questions help assess the usability and visual design of the app, ensuring it aligns with the expectations of general users.

Survey Questions
The survey is divided into technical and non-technical sections. It includes both closed ended (e.g., rating scales) and open-ended questions for richer feedback.

Technical Survey Questions

1. Do you think the application would benefit from using classes?
2. How would you rate the tidiness of the code?
3. Does the annotation of the application make the code more understandable?
4. Have you worked on an application/project like this?
5. What security measures would you recommend for safeguarding the user’s data?
6. If yes, do you have any feature recommendations?

These questions target those with software development experience. They explore areas such as **object-oriented design**, **code readability**, and **data security**.

Non-Technical Survey Questions
1. What age range are you?
2. Does the green colour scheme reflect energy-saving themes to you?
3. How would you rate the UI (1-5)?
4. Have you ever checked your carbon footprint?
5. Do you have any energy-saving devices at home?
6. Is the navigation within the app clear and simple?
7. Is the carbon footprint calculator easy to use?
8. Are the input fields in the calculator clear and understandable?
9. Does the app feel too complex for its intended use?
10. Do you have any concerns/complaints about the application?

These questions evaluate user perception, environmental awareness, and engagement, providing valuable insight into how well the application communicates its purpose and serves its audience.

**Technical Feedback Responses – Energy-Saving Application**

**1. Is the code well-commented and easy to follow?**
Yes, the code is fairly well-commented. Key functions, such as the carbon footprint calculator logic and energy usage tracking modules, include brief summaries describing their purpose. However, some of the helper methods and database interaction logic could benefit from more detailed comments. Overall, a developer familiar with C# would be able to follow the code with minimal confusion, but additional annotations—especially around calculation formulas and data retrieval—would improve clarity.

**2. Are the variable names descriptive and appropriate?**
Variable names are mostly descriptive and align with best practices. For instance, variables like `dailyEnergyConsumption`, `carbonEmissionsKg`, and `userProfileData` clearly represent their functions or contents. Some internal variables (e.g., loop counters like `x` or `temp1`) could be renamed to more meaningful terms to enhance readability, especially in functions that handle dynamic input or iterate over energy data entries.

**3. What’s the best approach to linking this code to the database?**
Currently, the application uses ADO.NET with SQL commands for data access, which works but is a bit verbose and prone to SQL injection if not carefully handled. A better approach might be to implement Entity Framework Core, which would simplify data manipulation using LINQ and abstract the SQL layer. This would also make the code more maintainable and easier to adapt if the data model evolves. Additionally, using environment variables or a secure configuration system (e.g., appsettings.json with user secrets) to manage connection strings would improve security.

**4. Are the carbon footprint calculations accurate and efficient?**
The carbon footprint calculator appears to use standard formulas, factoring in parameters such as electricity usage (in kWh), gas consumption, and transport data (e.g., vehicle mileage). The calculations are accurate from a logic standpoint and are structured to allow easy adjustments for different units or regional emission factors. However, efficiency could be improved by isolating repeated calculations into reusable utility methods. Also, including unit tests to validate different scenarios (e.g., low/high energy users, zero input) would enhance reliability and make debugging easier.

---

**Non-Technical Feedback Responses – Energy-Saving Application**

**1. Is the colour scheme visually appealing and appropriate?**
Yes, the colour scheme is very appropriate. The use of green shades throughout the interface instantly gives off an “eco-friendly” and energy-conscious vibe, which aligns well with the purpose of the app. The contrast between background and text is good, making it readable. The inclusion of icons and soft accent colours (like light blues and greys) helps break up the green and keeps the interface from feeling too monochrome or overwhelming.

**2. Does the user interface feel intuitive and easy to use?**
Overall, yes. The layout is simple and clearly designed with the user in mind. The main dashboard provides a clear summary of energy usage and estimated carbon footprint, and buttons are labeled in plain language (e.g., "Track Energy", "View Suggestions", "Calculate Footprint"). First-time users can figure out where to go without much trial and error. However, adding short tooltips or a brief onboarding guide could make things even smoother for users unfamiliar with the topic.

**3. Is it easy to navigate through the application?**
Navigation is quite smooth. The menu is persistent and logically structured, with sections like “Dashboard,” “Reports,” “Tips,” and “Profile” all easily accessible. The transitions between screens are fast, and users can return to the homepage with a single tap or click. The back button also works as expected, which adds to the feeling of control. It’s easy to find specific features like the calculator or daily energy summary.

**4. Does the overall application look too complex for everyday users?**
Not really. While it’s clear that there are multiple features available, the interface doesn’t feel cluttered or overly technical. Everything is broken down into steps, and the language is simple and non-technical. For example, the carbon footprint calculator asks for basic details in a step-by-step format, avoiding jargon. The app does a good job of making a complex subject more approachable. That said, older users or those less comfortable with technology might appreciate a "simple mode" or visual walkthrough.
