# Overview
* [Researching and Choosing Technologies](#researching-and-choosing-technologies)
    * [Programming Languages](#programming-languages)
    * [Machine Learning](#machine-learning)
    * [Databases](#databases)
* [Prototyping](#prototyping)
    * [Diagrams](#diagrams)
    * [Class and Function Signatures](#class-and-function-signatures)

# Choosing Technologies and Prototyping

Now that we've figured out an idea as well as fleshed out the details of what it should do by the end, let's start figuring out how we'll implement our project.

## Researching and Choosing Technologies

When it comes time to start developing your project, you'll first need to decide what kind of technologies you're going to be using.

### Programming Languages

The first decision you'll need to make is what programming language to use. There are dozens of popular languages available, each with their own strengths and weaknesses.

Here is a chart of some of the most common programming languages as well as their most common use cases:

| Language | Strengths | Common Uses |
| -------- | --------- | ----------- |
| Python   | Easy to learn, Access to community-built libraries | Web applications, Machine learning, Data retrieval and engineering|
| C/C++    | High performance, Low level control over memory | Resource intensive applications, Game engines, High-liability software (Medical, Military, etc.) |
| C# | Easier to use than C/C++ but less powerful | Full-stack web applications, Game development |
| Java     | Encourages object oriented programming | Android app development |
| Javascript| Powerful frameworks for website functionality | Advanced website development, Web applications |
| HTML/CSS | Pixel-by-pixel control over webpage appearance | Front-End Website Development |
| R | Fast and easy statistical computations | Data science and visualization |
| Ruby | Quick web-app development with Ruby-On-Rails | Web Applications |
| Swift | Designed specifically for iOS | iOS App Development |

If the project you're working on doesn't fall into any of these common use cases, try researching what programming languages are used by applications similar to your project.

### Machine Learning

Machine learning (or ML for short) is quickly becoming one of the most powerful tools in all of computing. However, knowing **when** to use it is just as important as knowing **how**.

ML algorithms are very good at a few key tasks: making predictions, recognizing patterns, identifying important information, and classifying objects.

To ensure that an ML algorithm performs each of these tasks with the highest accuracy possible, it must first be trained on a large pool of high quality data. This is one of the biggest limitations of Machine Learning, and it will generally be the deciding factor for whether or not you can properly implement it into your project.

If you want to predict a certain event, you'll need a large amount of data from the history of that event occurring. For example, in order to predict future stock prices for a company, you'll need to train your ML algorithm on the past few months or years of stock prices for that company to begin to get useful results.

Before starting to add ML to your project, stop to consider whether or not you are trying to perform one of these 4 tasks, and if you have enough data to make an accurate model.

Now that you know **when** to use ML, stop by our Machine Learning Workshop on October 19 to learn about **how** to start using it in your projects.

### Databases

If you're going to be storing large amounts of data for your project, it's important to decide what type of database you're going to be using. There are 2 major types of databases: **SQL** and **NoSQL**

#### SQL
 - **SQL** stands for Structured Query Language. SQL databases use pre-defined schemas to determine their layout, making them more complicated to set up but much more organized overall.

 - Data is placed into tables which can have relationships to other tables, allowing for connections to be made between similar data points like user IDs.

 - SQL itself is technically a programming language, so it can be very useful to learn.

 - There are a variety of engines for SQL databases, but MySQL is one of the most common. MySQL is supported by nearly every modern programming language, allowing you to incorporate your SQL database directly into your code. For mobile applications, check out SQLite.

#### NoSQL
 - **NoSQL**, just like the name implies, does not use Structured Query Language. There are no structured tables or relationships between tables, there is just data placed freely into formats like columns, graphs, or key-value pairs.

 - This simplicity makes NoSQL far easier to implement and a better choice for small, simple databases.

 - Just like with SQL, there are many different engines for implementing NoSQL. By far the most popular option is MongoDB, which is also supported by nearly every major programming language. 

Our Data Science Workshop on October 12 will have an introduction to SQL and MongoDB, so mark your calendar if you want to learn more!

## Prototyping
### Diagrams
When planning for a personal project, diagrams can be one of your most valuable tools. Mainly, they can help you to plan out how various parts of your program will interact with each other. For example, a diagram for a class may help you to specify the class variables and methods of that class. It can also help you to plan out class objects and instance variables. While class variables belong to a class, instance variables belong to an **instance** of that class, which is also known as an object.

For a powerful, free diagramming tool, check out [diagrams.net](https://www.diagrams.net/)!

### Class and Function Signatures
In programming you have things known as classes and functions. Classes are essentially blueprints for objects that will have certain characteristics or "instance variables" that are defined in that class. For example, a class may be "planet" and an instance variable may be "distance from the sun". A class signature is the line of code where the class is named and the parameters (instance variables) for that class are specified. Using classes will allow you to reuse the same "blueprint" for different parts of your program without having to rewrite the same code every time you need to use it.

Functions are used to carry out certain tasks on command when you run your program. Similar to a class signature, a function signature contains the name of the function and the parameters needed to complete that function. In certain programming languages, the function signature will also contain the return type for that function. Functions are another way to write reusable code and save time when making your program. By listing a certain set of instructions within a function, calling this function throughout the program will allow you to perform tasks without rewriting the code each time.

When planning for a personal project, try to outline what classes and functions you might need, and think about how they might interact with one another.


## Next section (recommended): [Clean Code](https://github.com/HackBinghamton/IntroToProgrammingWorkshop/blob/master/CleanCode.md)
