# MyLogReg
Let other people play with your logistic regression model.

## Examples
[Predict Getting into Harvard Law](https://www.mylogreg.netlify.com)

[Predict Heart Disease](https://www.mylogreg.netlify.com/heart.html)

[Predict Passing Exam](https://www.mylogreg.netlify.com/study.html)

[Predict Death Penalty](https://www.mylogreg.netlify.com/willbecharged.html)

![alt text](https://github.com/kaseyb002/MyLogReg/blob/master/public/assets/img/example.png "Harvard Calculator")

## Installation
Download/clone the repo.

Open the public/index.html file in a text editor.

Type your model into the config var at the top of the HTML file and fill out a few settings. 

Open the HTML file in a browser.

```javascript
/**************BEGIN EDITING HERE************/
var config = {
    headerTitle: "Harvard Law Admit Calcuator",//title at top of page
    resultsTitle: "Chance of Getting into Harvard Law",//explains results
    likelihoodLabel: "Likelihood of Admission",//shows along y-axis of graph
    intercept: -97.13444,//the intercept coefficient from your model
    variables: [
        {
            name: "LSAT",
            coefficient: 0.3172556,//your beta coefficient from the logistic regression model
            binary: false,//is this a YES/NO 1/0 variable?
            min: 120,//minimum that user can select for this variable (remove if binary)
            max: 180,//maximum that user can select for this variable (remove if binary)
            defaultValue: 170,//value that's already selected when the page loads (use true/false for binary)
            selectIncrement: 1,//how much to increment between min and max for user select (remove if binary)
            decimalPlaces: 0,//how many decimal places should be displayed (remove if binary)
            graphIncrement: 1,//determines the "ticks" on the graph's x-axis (remove if binary)
            graphAxisMin: 150,//bottom range for graph x-axis (remove if binary)
            graphAxisMax: 180//top range for graph x-axis (remove if binary)
        },
        {
            name: "GPA",
            coefficient: 11.05645,
            binary: false,
            min: 2.50,
            max: 4.00,
            defaultValue: 3.75,
            selectIncrement: 0.01,
            decimalPlaces: 2,
            graphIncrement: 0.10,
            graphAxisMin: 2.5,
            graphAxisMax: 4.0
        }
    ]
};
/*************STOP EDITING HERE**************/
```

### Inputting Binary Variables:
```javascript
{
	name: "Male",
	coefficient: 0.098,
	binary: true,
	defaultValue: false,
},
```
