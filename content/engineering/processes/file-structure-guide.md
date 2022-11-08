---
title: "File structure Guide"
date: 2021-08-31T18:11:15+02:00
draft: false
description: "File structure Guide"
weight: 3
---

### File Structure

To easily edit this table use the following link [tablesgenerator](https://www.tablesgenerator.com/markdown_tables#) and copy the markdown table into the editor.

| Type              | Description                                                                            | Location                       | Example                                                   |
| ----------------- | -------------------------------------------------------------------------------------- | ------------------------------ | --------------------------------------------------------- | --- |
| View              | User Interface                                                                         | Views/\<Context>/\<Name>       | Views/Auth/LoginView.xaml                                 |
| Model             | Business Objects that encapsulate data and behavior of application domain              | Models/\<Context>/\<Name>      | Models/Employee/EmployeeMail.cs                           |
| Data Access Model | Data transfer object for passing on values, ends in Obj                                | Models/\<Context>/\<Name>      | Models/Employee/EmployeeObj.cs                            |
| ViewModel         | Link between Model and View OR It Retrieves data from Model and exposes it to the View | ViewModels/\<Context>/\<Name>  | ViewModels/Auth/LoginViewModel.cs                         |
| Interface         | a syntactical contract that an entity should conform to                                | Interfaces/\<Name>             | Interfaces/User                                           |
| Control           | A Resuable UI Element                                                                  | UI/Controls/\<Context>/\<Name> | UI/Controls/Button/FlatButton.xaml                        |
| Service           | Responsible for sending HTTP requests to the API                                       | Services/\<Name>               | Services/Auth                                             |
| Utilities         | Helper Functions, Validation, Constants                                                | Utils/\<Context>/\<Name>       | Utils/Helpers/Case.cs Utils/Validations/UserValidation.cs |
| Assets            | Assets for UI elements e.g Pictures,Fonts etc                                          | Assets/\<Context>/\<Name>      | Assets/Fonts/Robot.Thin.tff                               |     |
