# JS30 #14: reference-vs-copy-in-js
This is yet another coding practice from JS30 series by Wes Bos.<br><br>
This exercise shows the difference between pass by value and by reference in primitive data types, arrays and objects by giving practical examples.
* Array copy methods 
```
const players = ['Wes', 'Sarah', 'Ryan', 'Poppy'];
const team2 = players.slice(); 
const team3 = [].concat(players); 
const team4 = [...players]; 
const team5 = Array.from(players);
```
* Object copy methods
```
const pandor = {
      species: "dog",
      breed: "golden retriever",
      name: "pandor",
      age: 12,
      breedCharacteristics: {
        isFriendly: true,
        isHappyWithOtherAnimalsAround: true
      }
    }
    
const toby = {...pandor}; //shallow copy of the object   
const murphy = Object.assign({}, pandor); // shallow copy of the object
const oscar = JSON.parse(JSON.stringify(pandor)); // deep clone method to copy deeper levels of the object

    
