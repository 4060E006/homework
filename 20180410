#include <iostream>
using namespace std;

int main()
{
  const int NUMBER_OF_ELEMENTS = 5;
  double numbers[NUMBER_OF_ELEMENTS];
  double sum = 0;

  for (int i = 0; i < NUMBER_OF_ELEMENTS; i++)
  {
    cout << "Enter a new number: ";
    cin >> numbers[i];
    sum += numbers[i];
  }

  double average = sum / NUMBER_OF_ELEMENTS;

  int count = 0; // The number of elements above average
  for (int i = 0; i < NUMBER_OF_ELEMENTS; i++)
    if (numbers[i] > average)
      count++;

  cout << "Average is " << average << endl;
  cout << "Number of elements above the average " << count << endl;
  system("pause");
  return 0;
}
