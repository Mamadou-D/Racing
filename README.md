# Racing
Simple game 

/*
    pseudocode for chapter 3 homework assignment

    create an array of strings with a size of 10.
    explain the story to the player, whatever story you wish to tell.
        the player starts with 3 items.
        over the course of several adventures, 
        1.  the player gains 3 items and has to name each of them.
            for example: BunnySword or FlameGuitar
             - because of cin limitations, the name can only be one word.
        2.  the player uses 1 item, making it go away.
        3. at each change in inventory - show the changes with a for loop that ignores strings that have "" no characters.
        
        For the final challenge, the player must give up their most treasured item to the bridge troll (or similar) to get past the bridge.
            The player will have to search for that item inside of a for loop.*/
            
            This is some requirements!!
            
           1. Beyond effort and polish (some of which is described below), here are some other things you can do.

   2. Send me a link in the comments to your assignment hosted publicly, like on github.com (good for showing off what you know to future employers)
    3. Create dialogue that makes the program feel more intuitive
    Use a while or do-while loop to ensure that the player successfully finds an item before moving past the bridge.
    
    I will save the written code below :
    
    #include <iostream>
#include <string>
#include<cstring>
#include <windows.h>

using namespace std;

int main()
{

     string invent [10];
     Sleep(300);
    cout << "\t\t\t\tWEL";
    Sleep(600);
    cout << "COME ! \n" <<endl;
     cout << "This is race battle, each player will start the run with 3 items to attack, defend or cure himself!!\nThose items can be anything you wish or mention  !!\n" <<endl;

     int num = 1;

 cout << "During the race, you dash 3 boxes and gains 3 new items. \nName each of them !!"<<endl;

 //1. I use for loop in order to not repeat the same code several time! so it helps me to get the name of  the 3 first items easily !!

     for (int i=0; i<3;i++){
        string itemsName;
        cin >> itemsName;
        invent[i]= itemsName;

        num++;
       }

   cout << "\nEach item has been stored into a specific space.\nLet's check them !\nHere are your items:\n";
       cout << "1- " << invent[0] << "\n2- " << invent[1] << "\n3- " << invent[2] << endl;

       cout << "\nYou keep going till you bump into an opponent.\nYou attack him directly to reduce his speed!!" <<endl;
       cout <<"\nYou attacked with :\t" << invent[0] << "\nWay to go !! Check your inventory." <<endl;
       invent [0]= invent [0]+ " empty box !";


        cout << "\nHere are your new items:\n";
       cout << "1- " << invent[0] << "\n2- " << invent[1] << "\n3- " << invent[2]<<endl;

       cout << "\nYou take a shortcut which leads you to BiggyStar's hideout!! "<< endl;
       cout <<"You finally find the super bonus item and store it in your inventory" <<endl;
       string bonusItem = "Grenade";
       invent [3]= bonusItem;

       cout << "\nYou choose to get rid of your:\t" <<invent[0]<< endl;
       invent[0]= "";
       cout << "\nYou arrive at a bridge where you must give up your most valued item before you get to FINISH LINE." <<endl;

// i declare a new string because i need one in my new for loop
          string newItem;
          /* This while loop will run the program as  long as it won't find any matching name.
          if you keep giving a wrong item name, the while loop will execute the program till you get one right name !*/

while (invent[1] != newItem && invent[2] != newItem && invent[3] !=newItem){
        cout << "What do you want to search for in your inventory !?\nItem:\t";
        cin >> newItem;

        cout <<"Searching";
        Sleep(2000);
        cout << ".";
        Sleep(2000);
        cout << ".";
        Sleep(2000);
        cout << ".!" <<endl;
        cout << "Here are your current Items:\n" <<endl;
        Sleep(2000);

       for (int i = 0; i < 10; i++ ){

            if (invent[i] == newItem){
                cout << "You have " << newItem << " in your inventory! You gets rid of * " << newItem << " * right away !!\n";
                cout << "- Empty bag of " + newItem <<endl;
        }

            else if (invent[i] != ""){
            cout << "- " << invent[i] << "\n";

            } else {

                   continue;
                }
       }

// i used if statement to help the program to print out the following message ! it was not necessary but interesting to see it recalling the user !
if (invent[1] != newItem && invent[2] != newItem && invent[3] !=newItem){
    cout << "\nSorry !! I can't find * " << newItem << " * in your inventory. Try again !!" <<endl;
}else{

    continue;}
}
cout << "You finally get to FINISH LINE and cross it !!" <<endl;

Sleep(1000);
cout << "\n\t°CON";
Sleep(700);
cout <<"GRA";
Sleep(700);
cout <<"TU";
Sleep(700);
cout << "LA";
Sleep(700);
cout <<"TIONS°\t" <<endl;
Sleep(300);





return 0;

}

