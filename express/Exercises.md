# Exercises

## Basic (Site)
* Create an express app.
* Have the app route to root and print to the browser some sort of inspiring message.
* Create a route for : *[Basic Routing](https://expressjs.com/en/starter/basic-routing.html)*
    - legal : Send to the browser the legal terms of your site
    - about : Send to the browser the info about your site
    - contact : Send to the browser contact information
* Ad a link from each page to each other page
* *Bonus* - Have the responses be it's own module with a full html document.
* *Super Bonus* - Add the same header and footer to every page without copying the code onto each page. *hint - You can use a function or modules*

## Medium (API)
* Create an express app.
* Have the App send only json responses. *hint - use res.json() in place of res.send()*
* Have the API have a route to "cats", "dogs", animals (both) returning all the data for each without using query strings. *hint filter() is your friend here*
* Have the API return a specifc id without using query strings.
* Using Query String return animals based on color, and age.
* *Bonus* - Add more functionality to your API including range for age, show only names, combining queries.
* *Super Bonus* - Make a small front end to consume your API.

```
[
{
            id:1,
            name:"Rainbow",
            age:3,
            color:'white',
            type:"cat"
        },
        {
            id:2,
            name:"Shadow",
            age:2,
            color:'brown',
            type:"cat"
        },
        {
            id:3,
            name:"puddles",
            age:4,
            color:'brown',
            type:"cat"
        },
         {
            id:4,
            name:"Sir Barks Alot",
            age:5,
            color:'black',
            type:"dog"
        },
         {
            id:5,
            name:"Daisy",
            age:6,
            color:'Yellow',
            type:"dog"
        },
        {
            id:6,
            name:"Molly",
            age:4,
            color:'white',
            type:"dog"
        }        
]
```