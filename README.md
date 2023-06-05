### Ex.08 Design of a Standard Calculator

### AIM:

To design a web application for a standard calculator with minimum five operations.

### DESIGN STEPS:

### Step 1:

Clone the github repository and create Django admin interface.

### Step 2:

Change settings.py file to allow request from all hosts.

### Step 3:

Use CSS for creating attractive colors.

### Step 4:

Write JavaScript program for implementing five different operations.

### Step 5:

Validate the HTML and CSS code.

### Step 6:

Publish the website in the given URL.

### PROGRAM : 
```
calculator.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=2.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="/static/css/styles.css"> 
    <title>Calculator</title>
</head>
<body>
    <div class="container">
        <h1>ARUVI CALCULATOR </h1> 

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button>(</button></td>
                    <td><button>)</button></td>
                    <td><button>C</button></td>
                    <td><button>%</button></td>
                </tr>
                <tr>
                    td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button>-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button>+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td> 
                    <td><button>.</button></td>
                    <td><button>/</button></td>
                    <td><button>=</button></td>
                </tr>
            </table>
        </div>
    </div>
</body>
<script src="/static/js/index.js"></script> 
</html> 

index.js

let screen = document.getElementById('screen'); 
buttons = document.querySelectorAll('button'); 
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue; 
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}

styles.css

.container{
    text-align: center;
    margin-top:23px
}

table{
    margin: auto;
}

input{
    border-radius: 30px;
    border: 5px solid red; 
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background:pink; 
    width: 102px;
    height: 90px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid yellow;
    background-color:red; 
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
    
}

h1{
    font-size: 28px;
font-family: 'Courier New', Courier, monospace;
}
```
### OUTPUT:

![image](https://github.com/Anandanaruvi/calc/assets/120443233/8a5f95fe-335f-49b8-9c92-25a856fa2d86)

![image](https://github.com/Anandanaruvi/calc/assets/120443233/abab5211-aeda-44db-b122-562f58fa7605)

### HTML VALIDATOR:

![image](https://github.com/Anandanaruvi/calc/assets/120443233/a27750ba-1f30-4dad-8271-d0acc4a7a3a8)

### RESULT:

The program for designing a standard calculator using HTML and CSS is executed successfully.
