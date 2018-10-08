#include <iostream>
#include <string>
using namespace std;

class Figure // Базовий клас
{
private:           //Завдання 5 в практичній №2   
	int* ChessDesk;//Завдання 5 в практичній №2
public:

	Figure(int cellsrows, int cellscols)   //Завдання 5 в практичній №2
	{	                                   //Завдання 5 в практичній №2
 		ChessDesk = new int[cellsrows];    //Завдання 5 в практичній №2
		for (int i; i < cellsrows; i++)    //Завдання 5 в практичній №2
		{                                  //Завдання 5 в практичній №2
			for (int j; j < cellscols; j++)//Завдання 5 в практичній №2
			{                              //Завдання 5 в практичній №2  
				ChessDesk[i][j];           //Завдання 5 в практичній №2 
			}                              //Завдання 5 в практичній №2
		}                                  //Завдання 5 в практичній №2
	}                                      //Завдання 5 в практичній №2

	~Figure()                              //Завдання 5 в практичній №2
	{                                      //Завдання 5 в практичній №2
		delete[] ChessDesk;                //Завдання 5 в практичній №2
		cout << "Об'єкти знищені" <<endl;  //Завдання 5 в практичній №2
	}                                      //Завдання 5 в практичній №2

	virtual void Beat() = 0; // В базовому класі створюємо віртуальний метод та присвоюємо йому 0, щоб виконати наслідування

	

	Figure()
	{
		lozung = "Знищити противника!";
	}
	Figure(string lozung) //Конструктор з параметром
	{
		this->lozung = lozung;
	}
	void Destroy()
	{
		cout << lozung << endl;
	}



	void Move();//Прототип функції класу "Queen"

private:

	string lozung;

};

class Horse :public Figure //Похідний клас
{
public:

	int number = 5;
	string color = "white";

};

class Pawn :public Figure //Похідний клас
{
public:

	int number = 2;
	string color = "black";

};

class Queen :public Figure //Похідний клас; в ньому виконую більшість завдань, які є в практичній роботі №2
{
public:

	Queen() :Figure("Підкоряюся лозунгу!")//За допомогою конструктора похідного класу змінюємо параметр конструктора базового класу
	{
		
	}

	void Beat() override // override допомагає мені не помилитися у написанні назви методу
	{
		cout << "Beat!" << endl;
	}
	void Move()
	{
		cout << "Move!" << endl;
	}
};

class Agregovaniyclass //Завдання 5 в практичній №2
{                      //Завдання 5 в практичній №2 
	Figure.N1(4,3);    //Завдання 5 в практичній №2
					   //Завдання 5 в практичній №2
};                     //Завдання 5 в практичній №2

void main()
{
	setlocale(LC_ALL, "rus");

	Queen a1;
	a1.Beat();

	Queen a2;
	a2.Move();

	cout << endl << endl;

	Queen A2;
	A2.Destroy(); //Реалізація базового конструктора за допомогою похідного

	Agregovaniyclass.implement; //Завдання 5 в практичній №2

	system("pause");
}
