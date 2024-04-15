```js
const player1_car = document.querySelector('#player1');
const computer_car = document.querySelector('#computer');

const race_btn = document.querySelector('#race_button');
const reset_btn = document.querySelector('#reset_button');
const result = document.querySelector('#result');

const initial_location_player1 = player1_car.offsetLeft;
const initial_location_computer = computer_car.offsetLeft;

let player1_location = initial_location_player1;
let computer_location = initial_location_computer;

let finish_line = player1_car.offsetLeft + 360;

reset_btn.disabled = true;

race_btn.addEventListener('click', function(){
    reset_btn.disabled = false;

    const player1_distance = Math.max(Math.floor(Math.random() * 81), 40); // Max movement of 80
    const computer_distance = Math.max(Math.floor(Math.random() * 81), 40); // Max movement of 80

    player1_location += player1_distance;
    computer_location += computer_distance;

    if (player1_location >= finish_line){
        player1_car.style.left = finish_line + 'px';
    } else{
        player1_car.style.left = player1_location + 'px';
    }

    if (computer_location >= finish_line){
        computer_car.style.left = finish_line + 'px';
    } else{
        computer_car.style.left = computer_location + 'px';
    }

    if(player1_location >= finish_line && computer_location < finish_line){
        result.textContent = 'You win!';
        race_btn.disabled = true;
    } else if(player1_location < finish_line && computer_location >= finish_line){
        result.textContent = 'You lose!';
        race_btn.disabled = true;
    } else if(player1_location >= finish_line && computer_location >= finish_line){
        result.textContent = "It's a draw";
        race_btn.disabled = true;
    } else{
        result.textContent = 'Race! Race! Race!';
    }

});

reset_btn.addEventListener('click', function(){
    player1_location = initial_location_player1;
    computer_location = initial_location_computer;

    player1_car.style.left = player1_location + 'px';
    computer_car.style.left = computer_location + 'px';

    result.textContent = 'Press "Race!" to begin!';
    race_btn.disabled = false;
    reset_btn.disabled = true;
});
```