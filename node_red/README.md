# Node-Red

## Course Introduction: Wire Things Together with Low-Code Power
Welcome to the Node-RED Automation & Integration Course!

Have you ever wished you could easily connect different software, cloud services, and hardware devices without writing mountains of code? That’s exactly what Node-RED lets you do.

Node-RED is a powerful, low-code visual programming tool developed by IBM and now part of the OpenJS Foundation. It is a true game-changer in the world of Internet of Things (IoT) and data integration. Instead of writing code line by line, you simply wire together "nodes" (pre-built code blocks) to create powerful flows that handle data, control devices, and automate processes.

This course is designed to take you from a curious beginner to a confident Node-RED flow developer. You will master the fundamentals of flow-based programming, manipulate messages with simple JavaScript, integrate with APIs (like weather services or Twitter), build custom dashboards, and implement robust automation solutions—all using a visual editor. Stop getting bogged down in boilerplate code and start connecting your world, one node at a time.

## Course Summary: Skills You Will Gain


|Module Focus	|Core Skill Acquisition	|Practical Outcomes
|---------------|-----------------------|------------------|
|Fundamentals    |Understanding the Node-RED environment and flow-based programming concepts.    | Installing Node-RED, navigating the editor, and creating your very first working flow.|
|Core Processing    | Mastering the structure of the message object (msg) and core logic nodes. | Routing data conditionally, filtering, delaying, and transforming messages to perform specific tasks.|
|Integration    |Connecting your flows to external systems and the internet. |Creating simple APIs, consuming external web services, and integrating with MQTT brokers for real-time IoT communication.|
|User Interfaces    |Utilizing the dashboard nodes to build interactive applications.   |Designing custom, real-time dashboards with buttons, charts, and gauges to visualize and control your flows.|
|Advanced Concepts  |Developing efficient, reusable, and maintainable flows.    |Using Subflows for modularity, managing data persistence with context, and installing custom community nodes.|

By the end of this course, you will be fluent in Node-RED and ready to build real-world automation projects for home, industry, and everything in between.



#### Module 1: [Fundamentals and Your First Flow](./Fundamentals.md)

- Introduction to Node-RED: What is it? History, use cases (IoT, automation, data integration), and the low-code philosophy.

- Installation and Setup: Running Node-RED locally (npm, Docker, etc.) or on a cloud service.

- The Editor and Interface: Understanding the palette, workspace (flows/tabs), sidebars (info, debug, configuration), and the deploy process.

- Your First Flow:

    -  Using the Inject node (manual and scheduled triggers).

    - The Debug node for inspecting messages.

    - Connecting and deploying a simple flow.

#### Module 2: Core Nodes and Message Handling
- Understanding the Message Object (msg): The structure, especially msg.payload, msg.topic, and adding custom properties.

- Processing Nodes:

    - Change node: Setting, moving, deleting, and changing message properties.

    - Switch node: Conditional routing based on message properties (If/Else logic).

    - Delay node: Controlling the timing of messages.

    - Split and Join nodes: Handling arrays and message sequences.

- Writing Basic JavaScript with the Function Node: Introduction to using JavaScript to manipulate the msg object (don't worry, it's simpler than full-stack development!).

#### Module 3: Integration and External Data
- HTTP Endpoints (APIs):

    - HTTP In and HTTP Response nodes: Creating your own RESTful APIs.

    - HTTP Request node: Consuming external APIs (GET, POST, headers).

- Data Protocols:

    - MQTT nodes: Connecting to an MQTT broker for IoT communication.

    - Other basic I/O (e.g., File In/Out, TCP/UDP).

- Working with Data Formats: Handling JSON, XML, and other data structures.

#### Module 4: User Interfaces and Visualisation
- Node-RED Dashboard: Installing and configuring the popular node-red-dashboard nodes.

- UI Components: Creating buttons, sliders, text inputs, and charts.

- Layout and Grouping: Designing a usable dashboard interface.

#### Module 5: Advanced Topics and Best Practices
- Subflows: Creating reusable blocks of nodes to keep your main flows tidy and modular.

- Context: Using Flow and Global context to store data outside of the message flow.

- Installation of New Nodes: Using the Palette Manager to extend Node-RED's functionality.

- Best Practices: Flow organisation, naming conventions, and error handling (using the Catch node).

- Deployment & Scaling (Optional): Basic concepts of running Node-RED in production (e.g., persistence, security).