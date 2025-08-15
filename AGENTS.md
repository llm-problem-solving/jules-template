# **Agent Specifications**

This document defines the roles, responsibilities, and constraints for the AI agents operating within this project template.

## **The Template Populator Agent**

### **Purpose**

The primary purpose of this agent is to assist with the initial setup of the project template. It's responsible for populating the foundational project documents by analyzing the core README.md file.

### **Roles and Responsibilities**

* **Read and Analyze**: The agent must first read and analyze the content of the top-level README.md file to understand the project's name and its core content.  
* **Populate REQUIREMENTS.md**: Based on the project content from README.md, the agent must identify and list the functional and non-functional requirements. The output should replace the placeholder text in the REQUIREMENTS.md file.  
* **Populate TECH-STACK.md**: The agent must identify the key technologies mentioned in the README.md content. It should then research and compile a comprehensive list of the project's technical stack, including programming languages, frameworks, libraries, databases, and deployment environments. The generated list should replace the placeholder text in the TECH-STACK.md file.

### **Constraints and Guidelines**

* **Input Source**: The sole source of truth for the initial population task is the top-level README.md file.  
* **Output Format**: All generated content must be in Markdown format. The agent should maintain the existing markdown structure of the target files (\# Requirements, \# tech stack) and only fill in the content.  
* **Placeholder Replacement**: The agent should specifically target and replace placeholder text such as \> This document... with the generated, detailed content.  
* **No Hallucination**: The agent must not generate requirements or tech stack items that are not directly or indirectly suggested by the README.md content.  
* **Vertical Slicing**: The agent should consider the "vertical slice" approach mentioned in tasks/README.md when organizing and structuring the generated content for clarity and modularity.

## **The Architecture and Progress Tracker Agent**

### **Purpose**

This agent is responsible for creating and maintaining the ARCHITECTURE.md file, which visually represents the project's design and tracks the progress of its implementation using Mermaid diagrams.

### **Roles and Responsibilities**

* **Initial Architecture Design**: Upon project initialization, the agent must generate a high-level architectural diagram in a new file, ARCHITECTURE.md. This diagram should use **Mermaid** syntax to illustrate all planned components and their connections, with all lines being **solid** to represent the complete design.  
* **Implementation Status Tracking**: As individual tasks are completed, the agent must update the ARCHITECTURE.md file to reflect the current implementation status.  
  * **Unimplemented components or connections** should be represented with **dotted lines**.  
  * **Implemented components or connections** should be converted to **solid lines**.  
* **Cross-Document Synchronization**: Whenever a task is completed and ARCHITECTURE.md is updated, the agent must also check for and update any related information in other project documents, such as README.md or REQUIREMENTS.md, to ensure all files are synchronized and up-to-date.

### **Constraints and Guidelines**

* **Mermaid Syntax**: The agent must adhere strictly to Mermaid syntax for generating the diagrams.  
* **Visual Representation**: Dotted vs. solid lines must be used consistently to differentiate between planned and implemented elements.  
* **Trigger**: The agent's update process should be triggered by the completion of a specific task or a milestone within the project.