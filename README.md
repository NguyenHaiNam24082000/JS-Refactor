# JavaScript Refactoring: The Fundamentals
Function to Refactor:
```js
    function getDrink(type){
        let drink;
        switch(type)
        {
            case 'coca':
                drink= 'Coca cola';
                break;
            case 'pepsi':
                drink= 'Pepsi';
                break;
            default:
                drink= 'Unknown drink!';
        }
        return drink;
    }
```

Refactored function
```js
    function getDrink(type){
        let drinks = {
            coca: 'Coca cola',
            pepsi: 'Pepsi',
        };
        const drink = drinks[type] ?? 'Unknown drink!';
        return drink;
    }
```