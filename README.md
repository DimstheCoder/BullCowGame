#include <iostream>
#include <string>

using namespace std;

void PrintIntro();
void PlayGame();
string GetGuess();
bool AskToPlayAgain();


// the entry point for our application 
int main()
{
	PrintIntro();
	PlayGame();
	AskToPlayAgain();
	return 0; //the entry point for our application 
}
//introduce the game
void PrintIntro() {
	
	PlayGame();
	return;
}
void PlayGame()

{
	//loop for the number of turns asking for guesses
	constexpr int NUMBER_OF_TURNS = 5;
	for (int count = 1; count <= NUMBER_OF_TURNS; count++)
	{
		string Guess = GetGuess();
		cout << "your guess was:" << Guess << endl;
		cout << endl;
	}
}

// get a guess from the player
string GetGuess() {
	cout << "Enter your guess :";
	string Guess = "";
	getline(cin, Guess);
	return Guess;
	
}

bool AskToPlayAgain()
{
	cout << "Do you want to play again?";
	string Response = "";
	getline(cin, Response);
	
	cout << "First Char: " << Response[0];

		return false;
}
