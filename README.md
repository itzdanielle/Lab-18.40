# Lab-18.40
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
 unsigned seed = time (0);
 srand (seed);

 int randNum;
 int guess;
 randNum = 1 + rand() % 100;


 cout << "Pick a number between 1-100" << endl;

int attempts = 0;
  do {
    cout << "your guess: " << endl;
    cin >> guess;
    attempts++;
    if (guess > randNum){
      cout << "Too High, try again" << endl;
    }
    else if (guess < randNum) {
      cout << "Too low, try again" << endl;
    }
    else {
      cout << "Congrats! You got it" << endl;
      cout << "Your total attempts are: " << attempts << endl;
    }
  
  }
 while (guess != randNum);

}
