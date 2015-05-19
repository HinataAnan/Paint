# Paint
float x,y,ex,ey,R,G,B,s;

void setup() {
  size(500,500);
  x =250;
  y =250;
  ex =50;
  ey =50;
  R = 0;//red
  G = 0;//green
  B = 0;//blue
  s = 1;
}

void draw() {
  //background(0,255,0);
  //fill(#1FEAFF);
  //noStroke();//sotowaku
  fill(R,G,B);
  rect(0,0,10,10);
  //ellipse(x,y,ex,ey);
  if (mousePressed && (mouseButton == LEFT)){
    ellipse(mouseX,mouseY,ex,ey);
    x +=0.1+(mouseX - x);
    y +=0.1+(mouseY - y);
  }
  /*if(ey>100){
    ex=100;
    ey=100;
  }
  if(ey<2){
    ex=2;
    ey=2;
  }*/
}
void keyPressed(){
  if(key == 'S'){
    s *=-1;
    if(s==1){
      stroke(0);
    }
    if(s==-1){
      noStroke();
    }
  }
  if(key == 'z'){
    ex=50;
    ey=50;
  }
  if(key == 'x'){
    ex=10;
    ey=50;
  }
  if(key == 'c'){
    ex=50;
    ey=10;
  }
  if(key == 'v'){
    ex+=1;
    ey+=1;
  }
  if(key == 'b'){
    ex-=1;
    ey-=1;
  }
  if(key == 'a'){
    R+=10;
  }
  if(key == 's'){
    G+=10;
  }
  if(key == 'd'){
    B+=10;
  }
  if(key == 'q'){
    R-=10;
  }
  if(key == 'w'){
    G-=10;
  }
  if(key == 'e'){
    B-=10;
  }
  if(key == '1'){
    save("Paint1.png");
  }
  if(key == '2'){
    save("Paint2.png");
  }
  if(key == '3'){
    save("Paint3.png");
  }
  if(key == '4'){
    save("Paint4.png");
  }
  if(key == '5'){
    save("Paint5.png");
  }
  if(key == '6'){
    save("Paint6.png");
  }
  if(key == '7'){
    save("Paint7.png");
  }
  if(key == '8'){
    save("Paint8.png");
  }
  if(key == '9'){
    save("Paint9.png");
  }
  if(key == '0'){
    save("Paint0.png");
  }
}
