# Woinshet Badicho Code Challenge

Great job on your project, Woinshet. Since we were not able to sync up and review your project together, we want to give you the opportunity to demonstrate your understanding of JavaScript in an asynchronous code challenge as an alternative to the Project Review. You will have 24 hours after acknowledging the receipt of this code challenge to complete and submit it. By reading this message, you are acknowledging that you have received these instructions and should begin working as soon as possible.

## Getting started

1. Read *all* of the instructions carefully.

2. Fork and clone the following repository onto your local machine: [Repo Link](https://github.com/thompsonplyler/basic-html-project)

## Once you have finished

Commit and push your changes to your fork like you would after completing a lab using the following commands in the code challenge directory:

- `git add .`
- `git commit -m "Completed assignment"`
- `git push`

## Goal of This Challenge

Filter the the book data response that you get back from the same API you used in your project (based on the number of pages). You will not have to add the filtered books to the DOM, you simply need to log the results in the browser's console. 

## Deliverables

1. As a user, I should be able to select a range of pages from a drop down list. The selections should be in increments of 100 pages from 0 - 1000. ex: (0-100, 100-200, 200-300, 300-400 etc...)

2. As a user, I should see a log in the browser's console of an array containing only book objects that match the selection from the dropdown. For example, if the '100-200' page range is selected in the dropdown, I should only see book objects that have a `numberOfPages` property value between 100 and 200 pages. Ex: 

```javascript
[{
    "url": "https://anapioficeandfire.com/api/books/6",
    "name": "The Sworn Sword",
    "isbn": "978-0785126508",
    "authors": [
        "George R. R. Martin"
    ],
    "numberOfPages": 152,
    "characters": [...],
    "povCharacters": []
}]
```

3. Copy the following code below in your code challenge's JavaScript file to get started (See starter code below):

```javascript
const api_url = "https://anapioficeandfire.com/api/books";
const response = await fetch(api_url);
    
const data = await response.json();
console.log(data);

const pageRanges = [
  "0-100",
  "100-200",
  "300-400",
  "500-600",
  "700-800",
  "900-1000"
];

const dropDown = document.createElement("select");

pageRanges.forEach((range) => {
  const option = document.createElement("option");
  option.textContent = range;
  dropDown.append(option);
});

dropDown.addEventListener("change", (e) => {
  console.log(e.target.value);
  // Code your solution here:



});

document.body.append(dropDown);
```
