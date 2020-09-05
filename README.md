# include<stdio.h>
#include<Windows.h>
int main(){
		int i;
		char name[100];         //使用之前要先复制 要轰炸的内容 
		printf("输入你要轰炸对象的名称：");
		scanf("%s" , &name , 40);
		printf("输入你要轰炸的次数：");
		scanf("%d",&i);
		HWND H =FindWindow(0,name);       //找对话窗口 
		while (i-- > 0){
			SendMessage(H,WM_PASTE,0,0);           //粘贴内容 
			SendMessage(H,WM_KEYDOWN,VK_RETURN,0); //回车发送 
		} 
 
} 
