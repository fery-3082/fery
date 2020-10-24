#include <GL/gl.h>
#include <GL/glu.h>
#include <GL/glut.h>

void display();

int main(int argc, char** argv)
{
    glutInit(&argc, argv);
    glutInitWindowSize(500,500);
    glutInitWindowPosition(500,500);
    glutCreateWindow("Hello World");
    glutDisplayFunc(display);
    gluOrtho2D(0,10,0,10);
    glutMainLoop();
}

void display()
{
    glClear(GL_COLOR_BUFFER_BIT);
    glMatrixMode(GL_MODELVIEW);
    glColor3f(1,0,1);
    glBegin(GL_POLYGON);
    glVertex2f(1,1);
    glVertex2f(3,2);
    glVertex2f(3,1);
    glVertex2f(1,2);
    glVertex2f(2,4);
    glEnd();
    glFlush();
}
Rey_00
Feryirawan123