# Introduction to Frameworks

A framework is a structured foundation that simplifies development by providing predefined architecture and reusable components, making applications easier to build, maintain, and scale.

![alt text](image-2.png)

- Reduces errors and code redundancy by promoting clean and organized code.
- Saves development time and cost with built-in tools and features.
- Allows customization and extension of functionalities as per project requirements.

<details>
    <summary><strong>Types of Frameworks</strong></summary>

Before starting development, you must choose the right programming language and framework based on your project requirements, scalability needs, and features.
![alt text](image-3.png)

- Select a programming language suitable for your project.
- Research frameworks within that language (e.g., Angular, Next.js, Vue.js for JavaScript).
- Compare features, performance, and community support.
- Clearly define requirements before finalizing the framework.
</details>

---

<details>
    <summary><strong>Web Development Frameworks</strong></summary>

Web development focuses on building and maintaining websites and web applications, including static, dynamic, and single-page applications. Web development frameworks provide essential tools, services, and APIs, and are mainly categorized into Front-end and Back-end frameworks.

<details>
    <summary><strong>1. Front-End Frameworks</strong></summary>

Frontend web development frameworks are used to create the user interface of the website that is seen and used by the users. They develop the client side of the application. Some of the popular front-end web development frameworks are Angular and Vue.js.

<details>
    <summary><strong>Angular</strong></summary>

Angular is an open-source TypeScript-based web framework developed by Google for building dynamic, scalable web applications and Progressive Web Apps (PWAs).

- Built with TypeScript and follows a component-based architecture.
- Provides high performance, strong tooling, and easy third-party integration.
- Used by major companies like Google, PayPal, Nike, and Upwork.
</details>

---

<details>
    <summary><strong>VueJS</strong></summary>

Vue.js is an open-source JavaScript frontend framework used for building interactive and dynamic user interfaces using HTML, CSS, and JavaScript.

- Follows the MVVM architecture and is easy to learn with strong community support.
- Used by companies such as Behance and Trustpilot.
</details>

---

<details>
    <summary><strong>Bootstrap</strong></summary>

Bootstrap is an open-source CSS framework used for developing responsive and mobile-first websites using HTML, CSS, and JavaScript.

- Enables fast, responsive, and cross-platform web development.
- Used by leading companies such as Airbnb, Netflix, and Uber.
</details>

</details>

---

<details>
    <summary><strong>2. Back-End Frameworks</strong></summary>
    
Backend web development frameworks operate on the server side and handle tasks such as processing requests, managing databases, and interacting with APIs. Popular examples include Ruby on Rails, Django, and PHP frameworks.

<details>
    <summary><strong>Ruby on Rails</strong></summary>
    
Ruby on Rails is an open-source Ruby-based web framework that follows the MVC architecture to build secure, scalable, and maintainable web applications.

- Based on the Model-View-Controller (MVC) architecture with support for third-party libraries.
- Used by companies such as CafePress and Airbnb.
</details>

---

<details>
    <summary><strong>Django</strong></summary>

Django is an open-source Python-based web framework designed for rapid development of secure, scalable, and maintainable web applications.

- Follows the Model-Template-View (MTV) architecture.
- Supports rapid development with built-in features like authentication and admin panel.
- Used by companies such as YouTube, Instagram, and Spotify.
</details>

---

<details>
    <summary><strong>Spring Boot</strong></summary>

Spring Boot is an open-source Java-based framework used to build production-ready, standalone, and scalable web applications.

- Simplifies application setup with auto-configuration and embedded servers.
- Provides high flexibility and scalability for enterprise applications.
</details>

</details>

---

<details>
    <summary><strong>Mobile Application Framework</strong></summary>

Mobile application frameworks are used to build apps for Android and iOS, supporting native, hybrid, and cross-platform development. Popular frameworks include Flutter, React Native, and Ionic.

<details>
    <summary><strong>Flutter</strong></summary>

Flutter is an open-source UI framework developed by Google for building cross-platform applications using the Dart programming language.

- Creates apps for Android, iOS, Web, and Desktop from a single codebase.
- Uses a widget-based architecture for fast and expressive UI development.
- Used by companies such as Google, Microsoft, Amazon, eBay, and Adobe.
</details>

<details>
    <summary><strong>React Native</strong></summary>
    
React Native is an open-source JavaScript framework developed by Meta for building cross-platform mobile and desktop applications using a single codebase.

- Supports Android, iOS, macOS, Web, and Windows platforms.
- Enables reusable components and faster development with JavaScript and React.
</details>
</details>

---

<details>
    <summary><strong>Data Science Frameworks</strong></summary>

Data Science is a field that collects data from various sources and then analyses them by applying various algorithms and statistics. Majorly, data scientists work with Python language hence many Python frameworks are used in data science:

<details>
    <summary><strong>PyTorch</strong></summary>

PyTorch is an open-source Python-based deep learning framework built on the Torch library for developing machine learning models.

- Used for building neural networks and deep learning models.
- Applied in NLP, image classification, and object detection tasks.
</details>

---

<details>
    <summary><strong>Apache Spark</strong></summary>

Apache Spark is an open-source big data processing framework used for large-scale data analytics and real-time data processing.

- Supports multiple languages including Scala, Python, Java, and R.
- Used for machine learning, real-time stream processing, and predictive analytics.
</details>

</details>

---

<details>
    <summary><strong>Other Frameworks</strong></summary>

Specialized frameworks target specific domains like gaming, machine learning, desktop, and API development.

<details>
    <summary><strong>Game Development</strong></summary>
    
- Unity: Unity used for developing 2D/3D games and VR experiences for mobile, PC, and consoles, adopted by companies like Ubisoft and Niantic.
- Unreal Engine: Unreal Engine used for creating AAA games, VR applications, and simulations, utilized by Epic Games and Square Enix.
</details>

---

<details>
    <summary><strong>Machine Learning</strong></summary>

- TensorFlow: TensorFlow is used for building and deploying machine learning models for tasks such as image recognition and NLP, and is used by companies like Google and Airbnb.
- Scikit-learn: Scikit-learn is used for data analysis and machine learning tasks such as classification and regression.
</details>

---

<details>
    <summary><strong>Desktop Application Development</strong></summary>
    
- Electron: Electron is used for building cross-platform desktop applications and powers apps like Visual Studio Code and Slack.
- Qt: Qt is used for developing high-performance desktop, embedded, and mobile applications with native interfaces, and is used by companies like Autodesk.
</details>

---

<details>
    <summary><strong>API Development</strong></summary>

- FastAPI: FastAPI is used for building high-performance APIs with automatic data validation and is used by companies like Microsoft and Uber.
- Express.js: Express.js is used for developing RESTful APIs and web applications and is used by companies like Twitter and Accenture.
</details>

</details>

---

<details>
    <summary><strong>Libraries Vs Frameworks</strong></summary>
    
Libraries provide specific reusable functionality, while frameworks offer a complete structured environment for building applications.

| Library | Framework |
| -------- | -------- |
| A collection of reusable functions or components for a specific task.   | A complete development structure with tools, libraries, and predefined architecture.   |
| Focuses on a particular functionality. | Covers the overall application development process. |
| Developer controls when and how to call it. | Controls the application flow and calls the developer’s code. |
| May be used independently or within a framework. | Often includes multiple libraries and tools. |

</details>

</details>