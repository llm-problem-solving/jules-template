# **Workromancer Store**

> AGENT MUST NOT EDIT THIS README.md
> AGENT MUST NOT WORK IN THIS DIRECTORY

This repository contains the necessary assets and information for listing an application on the [Workromancer Store](https://workromancer.ai/store).

**Important**: All build artifacts for your application must be managed through **GitHub Releases**.

## **Directory Structure**

The repository must follow the structure outlined below:

workromancer-store/  
├── README.md  
├── screenshots/  
│   ├── 01\_image.png  
│   ├── 02\_image.png  
│   └── ...  
├── APP\_INFO.yml  
└── app\_logo.png

## **File and Directory Guide**

### **1\. screenshots Directory**

This directory holds the images that will be displayed in the app's detail view on the store.

* **Purpose**: To provide users with a visual understanding of your application. The screenshots should clearly explain the features and user interface.  
* **Supported Formats**: png, gif, jpg, jpeg.  
* **Limit**: A maximum of 10 images can be displayed.  
* **File Naming Convention**: Files must be prefixed with a two-digit number (e.g., 01\_, 02\_) to set the display order.  
  * Example: 01\_main\_feature.png, 02\_dashboard\_view.jpg

### **2\. APP\_INFO.yml**

This YAML file contains the core metadata for your application listing.

* **Purpose**: To define the basic information displayed on the app list and detail pages.  
* **Required Fields**:  
  * version: The current version of your application (e.g., 0.0.1).  
  * name: The name of your application.  
  * description: A concise, one-line summary of what your application does.  
  * category: The type of application. Must be one of the following (lowercase only): app or saas.  
* **Example APP\_INFO.yml**:  
  version: 0.0.1  
  name: Workromancer  
  description: This is the store for what you want.  
  category: app
  os_requirements:
    - mac
    - window
    - iPadOS
    - Android

### **3\. app\_logo.png**

This is the official logo for your application.

* **Purpose**: To serve as the primary representative image for your app across the Workromancer Store.  
* **Format**: A high-quality png file is recommended.
