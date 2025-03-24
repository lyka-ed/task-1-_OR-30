## JSON Object Manipulation 
This script is about manipulating a json object and print it in a readable format. It follows the mockup sample HTML file making use of HTML, CSS and Javascript to present the result dynamically in a web browser.

## Aim
This script is aimed at processing the JSON objects, each aand representing it an article with properties `title`, `creation_date` and `page_id`. Transforming these data into a readable string - "Article "André Baniwa" (Page ID 6682420) was created at September 13, 2021." This will be displayed on the webpage alongside my javascript logic. 

## How my logic works
The `<script>` tag in the `index.html` file executes after DOM is fully loaed in the web browser.
The `data` variable is an array of objects that contains the; `title`, `page_id` and `creation_date`. Example:
`[
    {"page_id": 6682420, "creation_date": "2021-09-13", "title": "André Baniwa"},
          {"page_id": 4246775, "creation_date": "2013-12-10", "title": "Benki Piyãko"},
          {"page_id": 5882073, "creation_date": "2018-12-03", "title": "Célia Xakriabá"},
]`

# Implementation
I created a vairable named `months` that contains an array of months and defined a class `DataUtil` with three static methods to encapsulate the data processing logic:
- `formatDate(date)`: This takes date string and splits it into year, month and day using `split("-")`. Also convert numeric month using predefined `months` array. This also removes leading zeros from the dasy using `parseInt` and returns the formatted date ("September 12, 2021").
- `formatTitle(info)`: This uses `this.formatDate` to format the `creation_date` and returns a string in the format: "Article 'title' (Page ID page_id) was created on formatted_date".
- `formatAll(articles)`: this method now iterated over the `data` array using `.map(this.formatTitle.bind(this))` to process each object. It joins result with newlinecharacters(\n) for readability sake.

# Execution
- this script calls `DataUtil.formatAll(data)` to process the data array.
- Result is then logged to the console `console.log(result))` and display in the `<p id="results">` elemets using `document.getElementById("results").textContent = result`
  
## Features:
- OOP with class and static methods.
- JSON data into readable strings.
- My Javascript logic in a `<p id="code">` element.
- Display Result of my code output in a `<p id="results">` elements.
  
## How to start the script:
# Prerequistes
- Visual Studio Code with a live server extension installed.
- A web browser(e.g Brave, Chrome).

# Steps:
- Be sure that it is save as `index.html` or any other name you desire but `.html` must be attach.
- Open the file in VS Code.
- Start your live server ( bottom right corner of your vscode) by clicking on "Go Live" or open the file in a web browser.
- The web browser will display:
      - The formayyed JSON output in the `<p id="results">` element.
      - My Javascript logic in the `<p id="code">` element.

## Technologies used
- HTML
- CSS
- JavaScript

## Expected Output
Article "André Baniwa" (Page ID 6682420) was created at September 13, 2021.
Article "Benki Piyãko" (Page ID 4246775) was created at December 10, 2013.
Article "Célia Xakriabá" (Page ID 5882073) was created at December 3, 2018.
Article "Chirley Pankará" (Page ID 6977673) was created at October 5, 2022.
Article "Cristine Takuá" (Page ID 7069044) was created at February 16, 2023.
Article "Benki Piyãko" (Page ID 4246775) was created at December 10, 2013.
Article "Célia Xakriabá" (Page ID 5882073) was created at December 3, 2018.
Article "Chirley Pankará" (Page ID 6977673) was created at October 5, 2022.
Article "Cristine Takuá" (Page ID 7069044) was created at February 16, 2023.
