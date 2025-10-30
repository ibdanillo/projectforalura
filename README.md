# projectforalura
Project for class alura

let inimigoAltura = 50;
let personagemX = 200;
let inimigoX = 200;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  
  inimigoAltura = inimigoAltura + 1

  if(inimigoAltura > 400){
     inimigoAltura = 0;
   inimigoX = random([100,200,300])
    }
  distancia = dist(inimigoX, inimigoAltura, personagemX, 350);
  if(distancia < 50){
    textSize(32);
    textAlign(CENTER, CENTER);
    text("Game Over", 200, 200);
  console.log("Encostou");
    noLoop();
  }
  background("white");

  fill("black");
  circle(personagemX, 350, 50);

  fill("red");
  circle (inimigoX, inimigoAltura,50);    
}

function keyPressed(){
  console.log("tecla pressionada");
  //se teclapressionada = esquerda
  if(keyCode === LEFT_ARROW){
    personagemX = personagemX - 100
  }
  if(keyCode === RIGHT_ARROW){
  personagemX = personagemX + 100
  }
  personagemX = constrain(personagemX, 350, 50);
}      
