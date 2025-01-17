# Snake Game in C++
Snake game created using C++ and the graphics.h library.

![](images/menu.jpg)

![](images/in_game.png)

## Snake's body created using Doubly Linked List
![](images/snakes_body.jpg)

Logic for displaying the trailing body of the snake.

i)	Traverse the list till the end using next pointer.

ii)	From the last node, traverse back to the head by using previous pointer, while:

    head->x = head->prev->x
    head->y = head->prev->y
    
iii)	Now, we are back to the head node, display the squares by traversing back to the last node through next pointer.

iv)	Repeat the process till game is over, or is complete, or ESC is pressed.

## Forest Fire algorithm for polygon filling
![](images/forest_fire.jpg)

Queue Data Structure implemented using Linked List was used for implementing this algorithm for polygon filling.

```
while(head){
	r = deQueue(&head);
	colorBool = getpixel(r->x, r->y) == colorToRemove;

	if(r){ // i.e Not Null
		putpixel(r->x, r->y, colorToAdd);
	}
	if(colorBool){
		if(!inQueue(head, r->x+1, r->y))
			enQueue(&head, r->x+1, r->y);
		if(!inQueue(head, r->x-1, r->y))
			enQueue(&head, r->x-1, r->y);
		if(!inQueue(head, r->x, r->y+1))
			enQueue(&head, r->x, r->y+1);
		if(!inQueue(head, r->x, r->y-1))
			enQueue(&head, r->x, r->y-1);
	}
	delete r;
}
```
![image](https://github.com/user-attachments/assets/cb558655-9fad-4115-83f4-e5c3dc44a026)
![in_game](https://github.com/user-attachments/assets/2fa3045e-e4ff-48f1-881b-80f06bd96c5f)
![image](https://github.com/user-attachments/assets/e580430f-342a-4588-854a-9edcee5e672d)
![image](https://github.com/user-attachments/assets/e35248da-ef46-4445-9429-9d0c3ae7e86b)

