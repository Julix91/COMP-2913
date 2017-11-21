---
layout: page
title: Deliverables
permalink: /deliverables/
---

### Project 1 - To Do App

Weight: 25%

Due Date: Beginning of Class 5 (November 21st, 2017)

#### Requirements

1. Create a new React application, name it "todo-app".

1. This app will display a text input for the user, where they will be able to write a task.

1. A button should be displayed beside the input. When clicked, this button should add the user's input to a list of to do items.

1. Blank items should not be added to the list. This can happen if the user presses the "Add" button without writing down a task.

1. The list could potentially have 0 to multiple items.

1. Each list item must display a checkbox, and the task that the user wrote.

1. When checking off the checkbox, the list item should be removed from the list.

1. Ensure that you make use of Components intelligently. Think about what should be extracted into a separate component, and do so.

---

### Project 2 - Weather Application

Weight: 25%

Due Date: Beginning of Class 6 (November 28th, 2017)

#### Requirements

1. Create a new React application, name it "weather-app".

1. This app will display weather information for a select few cities.

1. Create a dropdown select input with at least 5 different cities. When selecting one of the cities from the dropdown, the view should display the weather information for that specific city.

1. You will need to make http requests to fetch for data. Documentation is here: [YAHOO! Weather API](https://developer.yahoo.com/weather/)

1. If you make the API request above, you will get data for the weather forecast for Vancouver, for the next few days. Display the forecast, with weather information, temperature, etc.

1. Users of your application should be able to use the dropdown to select different cities, and see weather for them.

1. Make good use of Component composition. Break parts of your application into sub-components, as you see fit.

1. Display images for each weather type. A rainy day should display a rainy icon.

1. The http request above returns data in American measurements. Since we're in Canada, ensure that the data displayed uses the metric system/Celsius. There are a number of ways to do this. It's up to you to figure out.

1. To facilitate your lives, I'll give you the specific endpoint that you need to make requests to.

```
# Note that there are invalid characters for an url on the API endpoint below.
# If you make a http request with these characters, the request utility will encode
# these characters automatically for you!
GET https://query.yahooapis.com/v1/public/yql?format=json&q=select * from weather.forecast where woeid in (select woeid from geo.places(1) where text="vancouver, bc")
```

---

#### Marking criteria

You will be marked according to the criteria below:

| Application works as requested | | 50%   |
| Clean, readable code           | | 25%   |
| Applied good structure         | | 15%   |
| Submitted project as requested | | 10%   |

---

#### Application works as requested

Does it meat all functional requirements?

---

#### Clean, readable code

Is the code clean and concise? Are the variables named appropriately? Does the code follow a standard? (eg. proper code line alignment, consistent standards). Is there commented out code that is not being used?

---

#### Submitted project as requested

Did you submit your files as specified and on time? Is your name on the project?

---

#### Submitting Project 1

In [D2L](http://learn.bcit.ca), look for the React course, and select Dropbox. There should be a folder named "Project 1".
Ensure that you **do not include** the node_modules folder in your project when submitting.
Zip your React app folder and name it project1_{firstName}_{lastName}.
Eg. project1_daniel_takeuchi.zip

---
