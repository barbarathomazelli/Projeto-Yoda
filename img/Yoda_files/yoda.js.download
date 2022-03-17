const img = document.getElementById( 'img' );
const buttons = document.getElementById( 'buttons' );
let colorIndex = 0;
let intervalId = null;

const trafficLight = ( event ) => {
    stopAutomatic();
    turnOn[event.target.id]();
}

const nextIndex = () => colorIndex = colorIndex < 2 ? ++colorIndex : 0;

const changeColor = () => {
    const colors = ['red','green','blue']
    const color = colors[ colorIndex ];
    turnOn[color]();
    nextIndex();
}

const stopAutomatic = () => {
    clearInterval ( intervalId );
}

const turnOn = {
    
    'red':   () => img.src = 'img/vermelho.jpg',
    'green':    () => img.src = 'img/verde.jpg',
    'blue':    () => img.src = 'img/azul.jpg',
    'automatic': () => intervalId = setInterval( changeColor, 80 )
}

buttons.addEventListener('click', trafficLight );
