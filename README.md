# calculator-javascript
calculator using  javascript
html css also used 

Q1) Draw a co-ordinate axis at the center of the screen
ANS:
#include <graphics.h>  // Include the graphics.h header file
#include <conio.h>

void main() {
    int gd=DETECT, gm, xcen, ycen; // Declare variables for graphics mode and center coordinates
    initgraph(&gd, &gm, "C:\\TURBOC3\\BGI"); // Initialize graphics mode

    xcen = getmaxx() / 2; // Calculate the x-coordinate of the center of the screen
    ycen = getmaxy() / 2; // Calculate the y-coordinate of the center of the screen

    // Draw a vertical line for the y-axis at the center of the screen
    line(xcen, 0, xcen, getmaxy());

    // Draw a horizontal line for the x-axis at the center of the screen
    line(0, ycen, getmaxx(), ycen);

    getch(); // Wait for a key press

    closegraph(); // Close the graphics mode
}

.
Q2) Write a program to implement 2D scaling.
Ans:

#include<conio.h>
#include<stdio.h>
#include<graphics.h>
void main()
{
float x1,x2,y1,y2,sx,sy;
int gd=DETECT,gm;
printf("\nEnter Start Cooridinate (x1,y1): ");
scanf("%f%f",&x1,&y1);
printf("\nEnter the End Cooridinate(x2,y2): ");
scanf("%f%f",&x2,&y2);
printf("'\nEnter Scaling Parmeters: ");
scanf("%f%f",&sx,&sy);
initgraph(&gd,&gm,"C:\\TC\\BGI");
line(x1,y1,x2,y2);
outtextxy(x1,y1,"Line Before Scaling");
x1=x1*sx;
y1=y1*sy;
x2=x2*sx;
y2=y2*sy;
line(x1,y1,x2,y2);
outtextxy(x1,y1,"Line After Scaling");
getch();
closegraph();
}



Q3) Write a program to perform 2D translation
Ans:
 #include<stdio.h>
#include<conio.h>
#include<graphics.h>
void main()
{
int gd=DETECT,gm;
float Tx,Ty,x1,y1,x2,y2;
printf("Enter the coordinates(x1,y1):");
scanf("%f%f",&x1,&y1);
printf("Enter the second coordinations(x1,y2)");
scanf("%f%f",&x2,&y2);
printf("Enter the translation parameter(Tx,Ty)");
scanf("%f%f",&Tx,&Ty);
initgraph(&gd,&gm,"C:\\TC\\BGI");
line(x1,y1,x2,y2);
outtextxy(x1,y1,"Before Translation");
x1=x1+Tx;
y1=y1+Ty;
x2=y2+Tx;
y2=y2+Ty;
line(x1,y1,x2,y2);
outtextxy(x2,y2,"After Translation");
getch();
closegraph();
}






Q4)Develop a simple text screen saver using graphics functions.
Ans:

# include<stdio.h>
#include<stdlib.h>
#include<graphics.h>
#include<conio.h>
#include<dos.h>
void main()

{
 int gd=DETECT,gm,col=480,row=640,font=4,size=8,direction=2,color=15;
 initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
 cleardevice();
 while(!kbhit())
 {
	settextstyle(random(font),random(direction),random(size));
	setcolor(random(color));
	outtextxy(random(col),random(row),"suraj");
	delay(25)  ;}
 closegraph();
}


Q5)Draw a simple hut on the screen.
ANS:

#include<graphics.h>
#include<conio.h>
void main(){
int gd=DETECT, gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
rectangle(150,180,250,300);
rectangle(250,180,420,300);
rectangle(180,250,220,300);
line(200,100,150,180);
line(200,100,250,180);
line(200,100,370,100);
line(370,100,420,180);
getch();
closegraph();
}

Q6) Divide your screen into four region, draw circle, rectangle, ellipse and half ellipse in each
Region
Ans:
#include<graphics.h>
#include<conio.h>

int main() {
    int gd=DETECT,gm,xcen,ycen;
    initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
    xcen=getmaxx()/2;
    ycen=getmaxy()/2;
   // Divide the screen into four regions
    line(xcen,0,xcen,getmaxy());
    line(0,ycen,getmaxx(),ycen);
    
    // Draw a rectangle
    rectangle(xcen+50,ycen-200,xcen+200,ycen-50);
    
    // Draw an ellipse
    ellipse(xcen-xcen/2,ycen+ycen/2,0,360,100,50);
    
    // Draw a half ellipse
    ellipse(xcen+xcen/2,ycen+ycen/2,0,180,100,50);
    
    // Draw a circle in one of the regions
    circle(xcen/2, ycen/2, 50);
 getch();
    closegraph();
    return 0;
}





Q7)Draw the following basic shapes in the center of the screen :


All in ine code:
#include<graphics.h>
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm,xcen,ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen=getmaxx()/2;
ycen=getmaxy()/2;
ellipse(xcen,ycen,0,360,100,50) ;
circle(xcen,ycen,50)  ;
rectangle(xcen-180,ycen-120,xcen+180,ycen+120) ;
rectangle(xcen-50,ycen-50,xcen+50,ycen+50);    //sqaure
circle(xcen,ycen,60);
circle(xcen,ycen,70);
circle(xcen,ycen,80);
line(0,ycen,getmaxx(),ycen) ;

getch();
closegraph();

}

i. Circle 
Ans:
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm,xcen,ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen=getmaxx()/2;
ycen=getmaxy()/2;
circle(xcen,ycen,200);
getch();
closegraph();
}


ii. Rectangle
Ans:
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm,xcen,ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen=getmaxx()/2;
ycen=getmaxy()/2;
rectangle(xcen-120,ycen-180,xcen+120,ycen+180);
getch();
closegraph();
}
 
iii. Square
Ans:
 #include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm,xcen,ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen=getmaxx()/2;
ycen=getmaxy()/2;
rectangle(xcen-200,ycen-200,xcen+200,ycen+200);
getch();
closegraph();
}

iv. Concentric Circles 
Ans:
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm,xcen,ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen=getmaxx()/2;
ycen=getmaxy()/2;
circle(xcen,ycen,30);
circle(xcen,ycen,50);
circle(xcen,ycen,70);
getch();
closegraph();
}

v. Ellipse 
Ans:
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm,xcen,ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen=getmaxx()/2;
ycen=getmaxy()/2;
ellipse(xcen,ycen,0,360,50,100);
getch();
closegraph();
}

vi. Line
Ans:
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm,xcen,ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen=getmaxx()/2;
ycen=getmaxy()/2;
line(0,ycen,getmaxx(),ycen) ;
getch();
closegraph();
}





Q8) Perform smiling face animation using graphic functions.
ANS:
#include<stdio.h>
#include<conio.h>
#include<graphics.h>
#include<stdlib.h>
#include<dos.h>
void main()
{
int gd=DETECT,gm,x=250,y=250;
initgraph(&gd,&gm,"C:\\TC\\BGI");
cleardevice();
while(!kbhit())
{
setfillstyle(SOLID_FILL,14);
fillellipse(x,y,100,100);
setfillstyle(SOLID_FILL,random(6));
fillellipse(x-30,y-30,20,40);
fillellipse(x+30,y-30,20,40);
setcolor(random(3));
ellipse(x,y+10,180,0,60,50);
delay(500);
}
closegraph();
}


Q9)Write a program using Flood Fill Algorithm. (4 and 8 connected)
ANS:

#include<graphics.h>
#include<conio.h>
#include<stdio.h>
#include<dos.h>
void flood(int,int,int,int);
void main()
{
int gd=DETECT,gm;
clrscr();
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
printf("\nCircle filled by flood fill algorithm");
circle(100,200,40);
flood(104,204,8,0);
getch();
}
void flood(int x,int y,int fill_col,int old_col)
{
if((getpixel(x,y)==old_col))
{
delay(1);
putpixel(x,y,fill_col);
flood(x+1,y,fill_col,old_col);
flood(x-1,y,fill_col,old_col);
flood(x,y+1,fill_col,old_col);
flood(x,y-1,fill_col,old_col);
}
}



8 connected:

#include<graphics.h>
#include<conio.h>
#include<stdio.h>
#include<dos.h>
void flood(int,int,int,int);
void main()
{
int gd=DETECT,gm;
clrscr();
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
printf("\nCircle filled by flood fill algorithm");
rectangle(50,80,100,120);
flood(54,104,8,0);
getch();
}
void flood(int x,int y,int fill_col,int old_col)
{
if((getpixel(x,y)==old_col))
{
delay(1);
putpixel(x,y,fill_col);
flood(x+1,y,fill_col,old_col);
flood(x-1,y,fill_col,old_col);
flood(x,y+1,fill_col,old_col);
flood(x,y-1,fill_col,old_col);

flood(x+1,y-1,fill_col,old_col);
flood(x-1,y-1,fill_col,old_col);
flood(x+1,y+1,fill_col,old_col);
flood(x-1,y+1,fill_col,old_col);
}
}




Q10) Write a program using Boundary Fill Algorithm. (4 and 8 connected)
ANs:

4:
#include<conio.h>
#include<stdio.h>
#include<graphics.h>
void boundary_fill(int x,int y,int fcolor,int bcolor)
{
if((getpixel(x,y)!=bcolor)&&(getpixel(x,y)!=fcolor))
{
putpixel(x,y,fcolor);
boundary_fill(x+1,y,fcolor,bcolor);
boundary_fill(x-1,y,fcolor,bcolor);
boundary_fill(x,y+1,fcolor,bcolor);
boundary_fill(x,y-1,fcolor,bcolor);
}}

void main()
{
int x,y,fcolor,bcolor;
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
printf("Circle fillby boundary fill: ");
printf("\n Enter the seed point (x,y): ");
scanf("%d%d",&x,&y);
printf("\n Enter the Boundary color: ");
scanf("%d",&bcolor);
printf("\nEnter New Color: ");
scanf("%d",&fcolor);
circle(102,152,45);
boundary_fill(x,y,fcolor,bcolor);
getch();
}

 



8:
#include<conio.h>
#include<stdio.h>
#include<graphics.h>
void boundary_fill(int x,int y,int fcolor,int bcolor)
{
if((getpixel(x,y)!=bcolor)&&(getpixel(x,y)!=fcolor))
{
delay(1);
putpixel(x,y,fcolor);
boundary_fill(x+1,y,fcolor,bcolor);
boundary_fill(x-1,y,fcolor,bcolor);
boundary_fill(x,y+1,fcolor,bcolor);
boundary_fill(x,y-1,fcolor,bcolor);
boundary_fill(x+1,y+1,fcolor,bcolor);
boundary_fill(x+1,y-1,fcolor,bcolor);
boundary_fill(x-1,y+1,fcolor,bcolor);
boundary_fill(x-1,y-1,fcolor,bcolor);
}}


void main()
{
int x,y,fcolor,bcolor;
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
outtextxy(50,50,"RECTANGLE FILLED BY fLOOD FILL:8-CONNECTER");
rectangle(50,80,100,120);
boundary_fill(52,82,15,6);
getch();
}


Q11)Develop the program for DDA Line drawing algorithm.
Ans:

#include <stdio.h>
#include <graphics.h>
#include <math.h>

int main() {
    int gd = DETECT, gm;
    float x1, y1, x2, y2, i, dx, dy, m;
    
    printf("\nEnter the x1 and y1 coordinate: ");
    scanf("%f%f", &x1, &y1);
    printf("\nEnter the x2 and y2 coordinate: ");
    scanf("%f%f", &x2, &y2);
    
    m = (y2 - y1) / (x2 - x1);
    
    initgraph(&gd, &gm, "C:\\TURBOC3\\BGI");
    
    // Drawing line using DDA algorithm
    for (i = x1; i <= x2; i++) {
        if (m < 1) {
            dx = x1 + 1;
            dy = y1 + m;
        } else if (m > 1) {
            dx = x1 + (1 / m);
            dy = y1 + 1;
        } else {
            dx = x1 + 1;
            dy = y1 + 1;
        }
        abs(dx)
         abs(dy)
        putpixel(dx, dy, 15);
        x1 = dx;
        y1 = dy;
        delay(50);
    }

    // Displaying the text "DDA line" beside the drawn line
    setcolor(RED);
    outtextxy((x1 + x2) / 2, (y1 + y2) / 2, "DDA line");

    getch(); // Wait for a key press before closing the window
    closegraph();

    return 0;
}

