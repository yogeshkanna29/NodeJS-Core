# Difference between dependencies, devDependencies and peerDependencies

Every web application project typically includes a file called package.json, which serves as a central repository for important project metadata. This file holds information such as dependencies, development dependencies, and peer dependencies, all of which are essential for managing the packages required to build, run, and maintain your project.

Understanding the differences between dependencies, devDependencies, and peerDependencies is crucial for managing project modules effectively.

<details>
    <summary><strong>Initializing a Project</strong></summary>
    
To initialize a new Node.js project, run the following command in your project’s root directory:

```bash
npm init -y
```

This creates a basic package.json file in your project directory.

</details>

---

<details>
    <summary><strong>1. Dependencies</strong></summary>
    
dependencies are libraries that your project needs in order to run in production. These are required for the core functionality of your application and must be installed for your application to work properly.

<details>
    <summary><strong>How to Add Dependencies</strong></summary>
    
To add a package as a dependency, use the following command:
```bash
npm install <package name>
```
Example: Installing the moment module for formatting the time in the project using the following command:  
```bash
npm install moment
```
After the module is installed, then if you navigate to the package.json file then you can find the moment with its version in the dependencies object as shown below:
```json
"dependencies": {   
   "moment": "^2.30.1",
}
```
- Production Use: These are essential for running the application in production.
- Automatic Installation: These packages are automatically installed when you run npm install.
</details>
</details>

---

<details>
    <summary><strong>2. devDependencies</strong></summary>
    
In package.json file, there is an object called as dev Dependencies and it consists of all the packages that are used in the project in its development phase and not in the production or testing environment with its version number. So, whenever you want to install any library that is required only in your development phase then you can find it in the dev Dependencies object.

<details>
    <summary><strong>How to Add devDependencies</strong></summary>
    
- To add a package as a development dependency, use the following command:
```bash
npm install <package name> --save-dev
```
Example: Installing the bootstrap module that we want to use in the development phase only and not in the production or testing phase for the project, use the following command:
```bash
npm install bootstrap --save-dev
```
package.json:
```json
"devDependencies": {
   "bootstrap": "^5.3.5",
}
```
- Development Use Only: These are only needed for development and testing, not in production.
- Automatic Installation: These packages are installed when you run npm install.
</details>
</details>

---

<details>
    <summary><strong>3. peerDependencies</strong></summary>

In package.json file, there is an object called as peerDependencies and it consists of all the packages that are exactly required in the project or to the person who is downloading and the version numbers should also be the same. That is the reason they were named as peerDependencies. The best example is 'react' which is common in every project to run similarly. 

<details>
    <summary><strong>How to Add peerDependencies</strong></summary>
    
You need to manually add peerDependencies in your package.json file. npm does not automatically install these dependencies.

```json
"peerDependencies": {
    "react": "^16.8.0"
}
```
- Compatibility: Specifies the compatible versions of other packages your project needs to work correctly.
- Manual Installation: npm will not install peerDependencies automatically. You must manually install them.
- Used in Published Packages: Peer dependencies are often used when you are developing a package that other developers will use in their projects.
</details>
</details>

---

<details>
    <summary><strong>Conclusion</strong></summary>
    
In a web development project Dependencies are needed for production, devDependencies are for development only, and peerDependencies ensure compatibility with specific versions of other packages, often used by plugins or shared libraries.
</details>

---