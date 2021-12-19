var ship;
var bullet;
var isClicked = true;
var commet;
var commet2;
var commet3;
var commet4;
var commet5;
var commetSpeed = 1;
var explode;
var bulRadius = 4;
var background;
var posX = Randomizer.nextInt(5,350);
var ptsCounter = 0;
var ptsText;
var livesCounter = 5;
var lifetxt;
var ptsicon;
var lifeicon;



function start(){
    backGround();
    spaceShip();
    makeCommet();
    makeCommet2();
    makeCommet3();
    makeCommet4();
    makeCommet5();
    lives();
    checkWall();
    pTs();
    
    colision();
    
}

function colision(){
    
    
     if(commet.getY()+commet.getHeight() <= ship.getY() || commet.getY()-commet.getHeight() <= ship.getY()
        || commet.getX() + commet.getWidth() >= ship.getX() ){
        var element = getElementAt(commet.getX(), commet.getY()+commet.getHeight());
        
        if(element == ship){
            remove(ship);
            remove(bullet);
        }
    
}
}

function lives(){
    
    lifetxt = new Text("5 ");
    lifetxt.setPosition(getWidth()-50,getHeight()-2);
    lifetxt.setColor(Color.yellow);
    add(lifetxt); 
    
    lifeicon = new WebImage("https://codehs.com/uploads/82aa6d03e4e38c49821c3c412b1400eb");
    lifeicon.setSize(25,30);
    lifeicon.setPosition(getWidth()-30,getHeight()-25);
    add(lifeicon); 
    
}

function pTs(){
    
    ptsText = new Text(" 0");
    ptsText.setPosition(30,getHeight()-2);
    ptsText.setColor(Color.yellow);
    add(ptsText);
    
    ptsicon = new WebImage("https://codehs.com/uploads/c622a1a0cb54a74f6b4217914316937b");
    ptsicon.setSize(25,25);
    ptsicon.setPosition(5,getHeight()-25);
    add(ptsicon);
}

function destroy(){
    //5
    if(bullet.getY()-bullet.getRadius() <= commet5.getY() || bullet.getY()+bullet.getRadius <= commet5.getY()
        || bullet.getX() + bullet.getRadius() >= commet5.getX() ){
        var element = getElementAt(bullet.getX(), bullet.getY()-bullet.getRadius());
        
        if(element == commet5){
            remove(commet5);
            remove(bullet);
            respawnCommet5();
            ptsCounter++;
    
        }
    }
    
    //4
    if(bullet.getY()-bullet.getRadius() <= commet4.getY() || bullet.getY()+bullet.getRadius <= commet4.getY()
        || bullet.getX() + bullet.getRadius() >= commet4.getX() ){
        var element = getElementAt(bullet.getX(), bullet.getY()-bullet.getRadius());
        
        if(element == commet4){
            remove(commet4);
            remove(bullet);
            respawnCommet4();
            ptsCounter++;
        }
    }
    
    // 3
     if(bullet.getY()-bullet.getRadius() <= commet3.getY() || bullet.getY()+bullet.getRadius <= commet3.getY()
        || bullet.getX() + bullet.getRadius() >= commet3.getX() ){
        var element = getElementAt(bullet.getX(), bullet.getY()-bullet.getRadius());
        
        if(element == commet3){
            remove(commet3);
            remove(bullet);
            respawnCommet3();
            ptsCounter++;
        }
    }
    
    // #2
    if(bullet.getY()-bullet.getRadius() <= commet2.getY() || bullet.getY()+bullet.getRadius <= commet2.getY()
        || bullet.getX() + bullet.getRadius() >= commet2.getX() ){
        var element = getElementAt(bullet.getX(), bullet.getY()-bullet.getRadius());
        
        if(element == commet2){
            remove(commet2);
            remove(bullet);
            respawnCommet2();
            ptsCounter++;
        }
    }
    
    // #1
    if(bullet.getY()-bullet.getRadius() <= commet.getY() || bullet.getY()+bullet.getRadius <= commet.getY()
        || bullet.getX() + bullet.getRadius() >= commet.getX() ){
        var element = getElementAt(bullet.getX(), bullet.getY()-bullet.getRadius());
        
        if(element == commet){
            remove(commet);
            remove(bullet);
            respawnCommet();
            ptsCounter++;
        }
    }
    
    ptsText.setText(ptsCounter);
    
    if(ptsCounter==50){
        gameWin();
        stopTimer(clickfire);
         stopTimer(fallingCommet);
         stopTimer(fallingCommet2);
         stopTimer(fallingCommet3);
         stopTimer(fallingCommet4);
         stopTimer(fallingCommet5);
         remove(ship);
         remove(commet);
         remove(commet2);
         remove(commet3);
         remove(commet4);
         remove(commet5);
         remove(lifeicon);
         remove(ptsText);
         remove(ptsicon);
         remove(lifetxt);
         mouseClickMethod(empty);
    }
}

function checkWall(){
    
    
    if( commet.getY() > getHeight() ){
        
        commet.setPosition(Randomizer.nextInt(15,350),-20);
        livesCounter--;
    }
    
    if( commet2.getY() > getHeight() ){
        
        commet2.setPosition(Randomizer.nextInt(15,350),-20);
        livesCounter--;
    }
    
    if( commet3.getY() > getHeight() ){
        
        commet3.setPosition(Randomizer.nextInt(15,350),-20);
        livesCounter--;
    }
    
    if( commet4.getY() > getHeight() ){
        
        commet4.setPosition(Randomizer.nextInt(15,350),-20);
        livesCounter--;
    }
    
    if( commet5.getY() > getHeight() ){
        
        commet5.setPosition(Randomizer.nextInt(15,350),-20);
        livesCounter--;
    }
     
     lifetxt.setText(livesCounter);
     
     
     if(livesCounter == 0){
         looserPanel();
         stopTimer(clickfire);
         stopTimer(fallingCommet);
         stopTimer(fallingCommet2);
         stopTimer(fallingCommet3);
         stopTimer(fallingCommet4);
         stopTimer(fallingCommet5);
         remove(ship);
         remove(commet);
         remove(commet2);
         remove(commet3);
         remove(commet4);
         remove(commet5);
         remove(lifeicon);
         remove(ptsText);
         remove(ptsicon);
         remove(lifetxt);
         mouseClickMethod(empty);
     }
     
     
     
    
}

function shipCheckWall(){
    
    if(ship.getX()+ship.getWidth() > getWidth()){
        ship.setPosition(getWidth()-ship.getWidth()+10, ship.getY());
    }
    
    if(ship.getX()-ship.getWidth() < -80){
        ship.setPosition(-8, ship.getY());
    }
    
    if(ship.getY()+ship.getHeight() > getHeight() ){
        ship.setPosition(ship.getX(), getHeight()-ship.getHeight());
    }
    
}

function shipMove(e){
    ship.setPosition(e.getX()-ship.getWidth()/2,e.getY()-ship.getHeight()/2);
    shipCheckWall();
    
}

function spaceShip(){
    
    ship = new WebImage("https://codehs.com/uploads/8bb4e1db3cb003bfd6b037e7bc4ef175");
    ship.setSize(70, 70);
    ship.setPosition(100,200);
    add(ship);
    mouseMoveMethod(shipMove);
    bulletAction();
}

function bulletAction(){
    
    mouseClickMethod(fire);
    mouseUpMethod(stopfire);
}

function fire(e){
var mySong = new Audio("https://codehs.com/uploads/475a3044da2fdee9ce4b9f9246156c35");
    mySong.play();
   isClicked != isClicked;
   if(isClicked == true){
      makeBullet();
    
    setTimer(clickfire,20);
    bullet.setPosition(ship.getX()+35,ship.getY());
   }
    
}

function makeBullet(){
    
    bullet = new Circle(bulRadius);
    bullet.setPosition(ship.getX(),ship.getY());
    bullet.setColor(Color.red);
    add(bullet);
    
}

function stopfire(e){
    stopTimer(clickfire);
    remove(bullet);
}

function clickfire(){
    bullet.move(0,-48); 
    
    bullet.setPosition(bullet.getX(),bullet.getY());
    destroy();
}

function backGround(){
    
    background = new WebImage("https://codehs.com/uploads/09c103fb170cbfc7a6a8c4427db8baa1");
    background.setSize(getWidth(),getHeight());
    add(background);
    
}

// კომეტა #1
function makeCommet(){
    
    commet = new WebImage("https://codehs.com/uploads/f350aba2913e1bf84e218978792f191d");
    commet.setSize(50,50);
    commet.setPosition(posX,-20);
    add(commet);
    
    setTimer(fallingCommet,20);
}

function fallingCommet(){
    commet.move(0,commetSpeed);
    checkWall();
}

function respawnCommet(){
    commet.setPosition(posX,-20);
    add(commet);
}

// კომეტა #2

function makeCommet2(){
    
    commet2 = new WebImage("https://codehs.com/uploads/f350aba2913e1bf84e218978792f191d");
    commet2.setSize(50,50);
    commet2.setPosition(Randomizer.nextInt(5,350),-20);
    add(commet2);
    
    setTimer(fallingCommet2,20);
}

function fallingCommet2(){
    commet2.move(0,commetSpeed);
    checkWall();
}

function respawnCommet2(){
    commet2.setPosition(Randomizer.nextInt(5,350),-20);
    add(commet2);
    
    
}

// კომეტა #3

function makeCommet3(){
    
    commet3 = new WebImage("https://codehs.com/uploads/f350aba2913e1bf84e218978792f191d");
    commet3.setSize(50,50);
    commet3.setPosition(Randomizer.nextInt(15,350),-20);
    add(commet3);
    
    setTimer(fallingCommet3,30);
}

function fallingCommet3(){
    commet3.move(0,commetSpeed);
    checkWall();
}

function respawnCommet3(){
    var min = Randomizer.nextInt(15,300);
    var max = Randomizer.nextInt(15,300);
    commet3.setPosition(Randomizer.nextInt(min,max),-20);
    add(commet3);
    
}

// კომეტა #4

function makeCommet4(){
    
    commet4 = new WebImage("https://codehs.com/uploads/f350aba2913e1bf84e218978792f191d");
    commet4.setSize(50,50);
    commet4.setPosition(Randomizer.nextInt(15,350),-20);
    add(commet4);
    
    setTimer(fallingCommet4,22);
}

function fallingCommet4(){
    commet4.move(0,commetSpeed);
    checkWall();
}

function respawnCommet4(){
    var min = Randomizer.nextInt(15,300);
    var max = Randomizer.nextInt(15,300);
    commet4.setPosition(Randomizer.nextInt(min,max),-20);
    add(commet4);
    
}

// კომეტა #5

function makeCommet5(){
    
    commet5 = new WebImage("https://codehs.com/uploads/f350aba2913e1bf84e218978792f191d");
    commet5.setSize(50,50);
    commet5.setPosition(Randomizer.nextInt(15,300),-20);
    add(commet5);
    
    setTimer(fallingCommet5,25);
}

function fallingCommet5(){
    commet5.move(0,commetSpeed);
    checkWall();
}

function respawnCommet5(){
    var min = Randomizer.nextInt(15,300);
    var max = Randomizer.nextInt(15,300);
    commet5.setPosition(Randomizer.nextInt(min,max),-20);
    add(commet5);
    
}

// წაგების ტექსტი
function looserPanel(){
    var gameover = new Text("Game Over Noob !!!", "30pt Arial");
    gameover.setPosition(getWidth()/2-gameover.getWidth()/2,getHeight()/2);
    gameover.setColor(Color.red);
    add(gameover);
}

function empty(){
    
}

function gameWin(){
    var gamewin = new Text("!! You Won !!!", "30pt Arial");
    gamewin.setPosition(getWidth()/2-gamewin.getWidth()/2,getHeight()/2);
    gamewin.setColor(Color.green);
    add(gamewin);
}
