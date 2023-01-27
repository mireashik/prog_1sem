https://lizochekk.jimdofree.com


---

### Компиляторы
http://www.codeblocks.org/downloads/binaries
<br>
https://github.com/Embarcadero/Dev-Cpp

### Огромное спасибо
- https://github.com/Vedji/Procedural_Programming_HomeWork
- https://github.com/vbg911/procedural-programming
- https://github.com/Nick648/C-plus-_Codes
- https://github.com/MintyRoma/PP_MIREA
- https://github.com/zubai69
- https://github.com/micr0chip/CompilerLAB7
- https://github.com/Kyinex/Homework
- https://github.com/ledhcg/Mos19_si2pls
- https://github.com/ViktorVlasov/Homework-Mirea
- https://github.com/NEK-RA/university-homeworks
- https://github.com/Alunchik
- https://github.com/soumirel/RTU_ProceduralProgramming_1stSemester_Task4
- https://github.com/Haze272/University-programming
- https://github.com/karpelevi4?tab=repositories
- https://github.com/Kreckeroff/1sem_PP
- https://github.com/Bigljuse/UniversityHomeWorkCPP

---

## Домашнее задание 1
### 1.1 Имя
```c++
#include <iostream>
using namespace std;

int main() {
    setlocale(LC_ALL, "Russian"); // вывод русских букв
    cout << "Имя";
    return 0;
}
```
### 1.2 Арифметика
```c++
#include <iostream>
using namespace std;

int main() {
    int a, b;
    cin >> a >> b;
    if (b == 0) {
        cout << "You cannot divide by 0";
    }
  
    cout << "a + b = " << a + b << endl;
    cout << "a - b = " << a - b << endl;
    cout << "a * b = " << a * b << endl;
    cout << "a / b = " << a / b << endl;
    return 0;
}
```

### 1.3 Уравнение
```c++
#include <iostream>
using namespace std;

int main() {
  int b, c;
  cin >> b >> c;
  if (b == 0) {
    cout << "division by zero" << endl;
    return 0;
  }
  
  int x = -c/b;
  cout << x;
  return 0;
}

```

### 1.3 Ещё одно уравнение

```c++
#include <iostream>
#include <math.h>
using namespace std;

int main() {
  int a, b, c;
  cout << "--------- \n";
  cout << "a = ";
  cin >> a;
  cout << "b = ";
  cin >> b;
  cout << "c = ";
  cin >> c;
  
  float d = (b*b)-4*a*c; // считаем d
  
  if (a == 0) { // если a = 0, то считаем линейное уравнение
    if (b == 0) {
    cout << "division by zero" << endl;
    main();
    }
  
  int x = -c/b;
  cout << "x = " << x << endl;
  main();
  }
  
  if (d < 0) { // если d < 0, то корней нет
    cout << "No solution" << endl;
    main();
  }
  else if (d == 0) { // если d = 0, то корень один
    cout << "x = " << (-b)/(2*a) << endl;
    main();
  }
  else {
    cout << "x1 = " << (-b + sqrt(d))/(2*a) << endl;
    cout << "x2 = " << (-b - sqrt(d))/(2*a) << endl;
    main();
  }

  return 0;
}
```

### 1.4 Лампа со шторой
Светло: день И раздвинуты шторы ИЛИ включена лампа
<br>
Светло ли в комнате?
```c++
#include <iostream>
using namespace std;

int main() {
  setlocale(LC_ALL, "Russian"); // вывод русских букв
  int time, curtains, lamp;
  cout << "Введите данные: \n";
  cout << "Про время суток (1 - день, 0 - ночь) \n";
  cout << "Про шторы (0 - раздвинуты, 1 - закрыты) \n";
  cout << "И лампу (1 - включена, 0 - выключена) \n";
  cin >> time >> curtains >> lamp;
  if (lamp == 1) {
    cout << "В комнате светло \n";
  }
  else if (time == 1 and curtains == 0) {
    cout << "В комнате светло \n";
  }
  else {
    cout << "В комнате темно \n";
  }

  return 0;
}

```
## Домашнее задание 2

### 2.1 Конус
```c++
#include <iostream>
#include <math.h>
using namespace std;

int main() {
    double R; // нижнее основание
    double r; // верхнее основание
    double h;
    
    cout << "R = ";
    cin >> R;
    cout << "r = ";
    cin >> r;
    cout << "h = ";
    cin >> h;
    cout << "---------\n";
    if (R <= 0 or r <= 0 or h <= 0) {
      cout << "No solution!\n";
      main();
    }
    float l = sqrt(pow(R, 2) + pow(h, 2));
    float S = M_PI * (pow(R, 2) + (R + r) * l + pow(r, 2));
    float V = 0.3333333333 * M_PI * h * (pow(R, 2) + R * r + pow(r, 2));
    cout << "l = " << l << endl;
    cout << "S = " << S << endl;
    cout << "V = " << V << endl;
    return 0;
}
// 3 2.5 8.016
```

### 2.2 Развлетвление
```c++
#include <iostream>
#include <cmath>
using namespace std;

int main() {
    double x;
    double a;
    double w;
    cin >> x >> a;
    if (x == 0) {
      cout << "x cannot be equal to 0" << endl;
    }
    else if (abs(x) < 1) {
      w = a * log(abs(x));
      cout << w << endl;
    }
    else if (a - pow(x, 2) < 0) {  // важно чтобы эта проверка шла перед корнем
      cout << "You cannot extract the root of a negative number" << endl;
    }
    else {
      w = sqrt(a - pow(x, 2));
      cout << w << endl;
    }
}
```

### 2.3 Функция
```c++
#include <iostream>
#include <math.h>
using namespace std;

int main() {
    double x, y, b, z;
    
    cout << "x = ";
    cin >> x;
    cout << "y = ";
    cin >> y;
    cout << "b = ";
    cin >> b;
    
    if (b - y <= 0 or b - x < 0) {
        cout << "the coefficient of log() cannot be less than or equal to 0 OR the root cannot be extracted from a negative number";
    }
    else {
    	z = log(b - y) * sqrt(b - x);
    	cout << "z = " << z;
	}

    return 0;
}
```

### 2.4 Порядок
```c++
#include <iostream>
using namespace std;


int main() {
    int N;
    
    cout << "N = "; // ввод переменных
    cin >> N;
    
    if (N <= 0) { // проверка что N натуральное число
        cout << "N is not natural number";
        return 0;
    }
    
    for (int i = 0; i < 10; i++) { // вывод 10 натуральных чисел
        cout << N++ << endl;
    }
    
    return 0;
}
```

### 2.5 Табуляция
```c++
#include <iostream>
#include <math.h>
using namespace std;

int main() {
    float x, y;
	for (x = -4; x <= 4; x += 0.5) { // изменение X от -4 до 4 с шагом 0.5
		y = (x * x - 2 * x + 2) / (x - 1); // функция

		if (x - 1 == 0) { // проверка деления на нуль
			cout << "y(" << x << ") = " << "division by zero!" << endl;
		}
		else {
			cout << "y(" << x << ") = " << y << endl;
		}
	}
    return 0;
}
```

## Домашнее задание 3
### 3.1 «Заем»
Месячная выплата m по займу в S рублей на n лет под процент p вычисляется по формуле

![изображение](https://user-images.githubusercontent.com/70198995/193253807-93376b73-5d95-4ee6-8386-9a82694b2de6.png)

```c++
#include <iostream>
#include <math.h>
using namespace std;

int main() {
double S; 
double p;
double n;
double r;
double m;
cout << "----------------------- \n";
cout << "S = ";
cin >> S;
cout << "p = ";
cin >> p;
cout << "n = ";
cin >> n;
  
if (S <= 0) {
  cout << "Numbers cannot be less than zero! \n";
  main();
  }

else if (p == 0) {
  m = S / (12 * n);
}

else {
  r = p / 100;
  m = S * r * pow(1 + r, n) / (12 * (pow(1 + r, n) - 1));
}

if (12 * (pow(1 + r, n) - 1) < 0) {
  cout << "You can't divide by 0! \n";
  main();
  }

cout << "m = " << m << endl;
main();
}
```

### 3.2 «Ссуда»
Под какой процент p выдана ссуда величиной S рублей, которая гасится месячными выплатами величиной m в течение n лет. Формула приведена в предыдущей задаче.

```c++
#include <iostream>
#include <math.h>
using namespace std;

int main() {
double S; // начальная ссуда S рублей
double n; // в течении n лет
double mTest; // месячная выплата mTest
double m; // заданная под условие с выплатами r
double r;
double rTemp = 0.0001; // временное r для вычисления
cout << "----------------------- \n";
cout << "S = ";
cin >> S;
cout << "n = ";
cin >> n;
cout << "mTest = ";
cin >> mTest;
  

if (n == 0 or S <= 0) { // на 0 делить нельзя!
  cout << "Incorrect years or amount of credit! \n";
  main();
  }

while (m < mTest) { ////// находим когда выплаты будут больше заданного, и выводим нужный %
  r = rTemp;
  m = S * r * pow(1 + r, n) / (12 * (pow(1 + r, n) - 1)); // подсчёт m с течением времени
  rTemp = rTemp + 0.0001;
  }

cout << "p = " << r * 100 << "%" << endl;  
main();
}
```

### 3.3 «Копирование файла»
Создать на диске текстовый файл и скопировать его на экран.

```c++
#include <iostream>
#include <fstream>
#include <string.h>
using namespace std;

int main() {
setlocale(LC_ALL, "rus"); // корректное отображение Кириллицы
char readline[30]; // буфер промежуточного хранения считываемого из файла текста
ifstream fin("33.txt"); // открыли файл для чтения
while (fin.getline(readline, 30)) {
  for (int i = 0; i < strlen(readline); i++) { // пробегание по кол-ву символов строки
    cout << readline[i];
  }
  cout << "\n"; // перенос на другую строку
}
fin.close();
return 0;
}
```
### Другое решение
```c++
    fstream fileStream;
    fileStream.open("33.txt");

    char readline[30];
    if (fileStream.fail()) {
        cout << "file not exist";
        ofstream fout("33.txt");
    }
    else {
        cout << "nice";
        ifstream fin("33.txt");
        while (fin.getline(readline, 30)) {
          for (int i = 0; i < strlen(readline); i++) {
            cout << readline[i];
          }
          cout << "\n";
        }
        fin.close();
    }
```

### 3.4 «Фильтр»
Вывести на экран только числа из созданного Вами на диске текстового файла, содержащего буквы и числа.

```c++
#include <iostream>
#include <fstream>
#include <string.h>
using namespace std;

int main() {
  setlocale(LC_ALL, "rus"); // корректное отображение Кириллицы
  char readline[30]; // буфер промежуточного хранения считываемого из файла текста
  ifstream fin("33.txt"); // открыли файл для чтения
  while (fin.getline(readline, 30)) {
    
    for(int i = 0; i < strlen(readline); i++) {
      if (isdigit(readline[i]) or readline[i] == '-' or readline[i] == ',' or readline[i] == '.') { // проверка на число
        cout << readline[i];
      }
    }
    
    cout << "\n"; // перенос на другую строку
    
  }
  fin.close();
}
```

### 3.5 «Сортировка букв»
Задать строку из 30 букв и расставить их в алфавитном порядке.

```c++
#include <iostream>
#include <fstream>
#include <string.h>
#include <algorithm>
using namespace std;

int main() {
  setlocale(0, "");
  string x;
  int i = 0;
  cout << "----------------------- \n";    
  getline(cin, x); // функция скушает строки с пробелами
  
  
  for (int i = 0; i < x.length() - 1; i++) {
    for (int j = i; j < x.length() - 1; j++) { 
      if (x[i] > x[j + 1]) {
        swap(x[i], x[j + 1]);
        }
      }
  }
  cout << x.substr(count(x.begin(), x.end(), ' '), x.length()) << endl; // конструкция чистит пробелы " "
  main();
```

## Домашнее задание 4
### 4.1 «Файл»
Создать файл, записать в него 10 чисел, закрыть, потом вновь открыть файл и найти сумму чисел.

Ввод в консоли!

```c++
#include <iostream>
#include <fstream>
using namespace std;

int main() {
  int i = 0; // кол-во цифр
  double sum = 0; // сумма
  double digital = 0;
  
  ofstream file("41.txt");
  while (i != 10) { // ввод чисел
  	i += 1;
  	cout << i << ") ";
  	if (cin >> digital) { // проверка на число
  		file << digital << "\n"; // запись в файл
	  }
	else {
		cout << "Incorrect input!" << endl;
		return 0;
	}
  }
  file.close();
  
  ifstream ifile("41.txt");
  while (i != 20) { // сумма чисел
  	ifile >> digital; // чтение из файла
    sum += digital; 
    i += 1;
  }
  ifile.close();
  
  cout << "SUM = " << sum << endl;
  return 0;
}
```

### 4.2 «Знак числа»
Определить знак введенного с клавиатуры числа, использовав подпрограмму-функцию
<br>
sign x =
<br>
1, x > 0
<br>
0, x = 0
<br>
-1, x < 0

```c++
#include <iostream>
using namespace std;

int sign(float x) {
    if (x > 0) {
	  return 1;
    }
    else if (x == 0) {
      return 0;
    }
    return -1;
}
  
int main() {
  double x = 0;
  cout << "----------------\n";
  cout << "x = ";
  if (cin >> x) {
  	cout << sign(x) << endl;
 	main();
  }
  else {
  	cout << "Incorrect input!";
  	return 0;
  }
}
```

### 4.3 «Геометрические фигуры»
Вычислить площади прямоугольника, треугольника, круга, используя подпрограммы-функции.

Функции! Оператор `switch case` чтобы выбрать площадь какой фигуры найти

**Неправильно найдена площадь (надо через 3 стороны + не забыть проверку)**

```c++
#include <iostream>
#include <cmath>
using namespace std;

double a, b, h, r;
double rect(double a, double b) { // прямоугольник
	if (a <= 0 || b <= 0) {
		return -1;
	}
	return a * b;
}

double trin(double a, double h) { // треугольник
	if (a <= 0 || h <= 0) {
		return -1;
	}
	return 0.5 * a * h;
}


double circle(double r) { // круг
	if (r <= 0) {
		return -1;	
	}
	return M_PI * pow(r, 2);
}

int main() {
	int select;
	cout << "-----------------------\n";
	cout << "1 (reactagle) / 2 (trinagle) / 3 (circle): ";
	cin >> select;
	switch (select) {
		case 1: // прямоугольник
			cout << "a = ";
			cin >> a;
			cout << "b = ";
			cin >> b;
			cout << "S reactagle = " << rect(a, b) << endl;
			main();
		case 2: // треугольник
			cout << "a = ";
			cin >> a;
			cout << "h = ";
			cin >> h;
			cout << "S trinagle = " << trin(a, h) << endl;
			main();
		case 3: // круг
			cout << "r = ";
			cin >> r;
			cout << "S circle = " <<  circle(r) << endl;
			main();
	}
}
```

**"Правильный" вариант (для этого предмета)** 

```c++
#include <iostream>
#include <cmath>
using namespace std;

double a, b, c, h, r, p;
double rect(double a, double b) { // прямоугольник
	if (a <= 0 or b <= 0) {
		return -1;
	}
	return a * b;
}

double trin(double a, double b, double c) { // треугольник (по 3 сторонам)
	if (a <= 0 or b <= 0 or c <= 0 or a + b <= c or a + c <= b or b + c <= a) {
		return -1;
	}
	p = (a + b + c) / 2;
	return sqrt(p * (p - a) * (p - b) * (p - c) );
}


double circle(double r) { // круг
	if (r <= 0) {
		return -1;	
	}
	return M_PI * pow(r, 2);
}

int main() {
	int select;
	cout << "-----------------------\n";
	cout << "1 (reactagle) / 2 (trinagle) / 3 (circle): ";
	cin >> select;
	switch (select) {
		case 1: // прямоугольник
			cout << "a = ";
			cin >> a;
			cout << "b = ";
			cin >> b;
			main();
		case 2: // треугольник
			cout << "a = ";
			cin >> a;
			cout << "b = ";
			cin >> b;
			cout << "c = ";
			cin >> c;
			cout << "S trinagle = " << trin(a, b, c) << endl;
			main();
		case 3: // круг
			cout << "r = ";
			cin >> r;
			cout << "S circle = " <<  circle(r) << endl;
			main();
	}
}
```

### 4.4 «Былая слава».
В 1912 году американский флаг «Былая слава» имел 48 звезд (по одной на
каждый штат) и 13 полос (по одной на колонию). Напечатать «Былую славу 1912 года».

![изображение](https://user-images.githubusercontent.com/70198995/193248925-827446be-2288-4cc1-b111-3bcdec04399d.png)

**Неправильно, но работает (циклы нельзя с готовыми строками нельзя)**
```c++
#include <iostream>
using namespace std;

int main()
{

    for (int i = 0; i < 7; i++) { // 7 верхних полос и 48 звёзд
        cout << "  *  *  *  *  *  *";
        cout << "__________________________" << endl;
    }

    for (int i = 0; i < 6; i++) { // 6 нижних полос
        cout << "____________________________________________" << endl;
    }
    return 0;
}
```

**Нелучший, но работающий вариант**
```c++
#include <iostream>
using namespace std;

int main() {
    char flag[13][30];

	for (int x = 0; x < 7; x++) {
		for(int y = 0; y < 6; y++) {
			flag[x][y] = '*';
		}
	}

	for (int x = 0; x < 7; x++) {
		for(int y = 6; y < 30; y++) {
			flag[x][y] = '_';
		}
	}

	for (int x = 7; x < 13; x++) {
	    for (int y = 0; y < 30; y++) {
	        flag[x][y] = '_';
	    }
	    cout << endl;
	}	

	// Вывод
	for (int x = 0; x < 13; x++) {
	    for (int y = 0; y < 30; y++) {
	        cout << flag[x][y];
	    }
	    cout << endl;
	}

}
```

### 4.5 «Синусоида».
Напечатать график функции у = sin x.

1. Обычные циклы
2. Windows.h (SetPixel, SetConsoleCursorPosition, CreatePen)

![изображение](https://user-images.githubusercontent.com/70198995/193249135-3cb55092-dcfc-4189-a115-728d0da40ff3.png)

Как вариант: https://gist.github.com/vocalinternet/ae8e39a7dbcf3c79ee784539063a1c1a

```c++
#include <iostream>
#include <windows.h>
#include <cmath>
using namespace std;

int getSin(double x, int d_y = 25) {
    return  (int) ((sin(x) * 10) + d_y/2);
}

void gotoxy(int x, int y) {
    COORD xy;
    xy.X = x;
    xy.Y = y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), xy);
}


int main() {
    for (double x = -10; x < 10; x+=0.1) {
        int y = getSin(x);
        if (y <= 1) {
			continue;	
		}
        gotoxy((int) (x * 10), y);
        cout << '*';
    }
    for (int i = 0; i < 120; i++) {
        gotoxy(i, 0);
        cout << ' ';
    }
    gotoxy(0, 26);
}
```

```c++
#include <cmath>
#include <iostream>
#include <string>
#include <vector>
using namespace std;

int main()
{
  int size = 100; // ширина графика
  int height = 21; // высота

  vector<string> sinGraph(height, string(size, ' ')); // пустое поле
  sinGraph[height/2] = string(size, '-'); // ось

  for(int i = 0; i < size; i++) { // точки графика
    sinGraph[(round(10 * sin(i / 4.5) + 10))][i] = '*'; 
  }
  
  for(auto s: sinGraph) { // напечатать 
    cout << s << '\n';
  }
}
```

### 4.6 «Автоматный распознаватель».
Декодировать римскую запись числа, состоящего из любого количества знаков. 
<br>
Правила: I -> 1, V -> 5, X -> 10, L -> 50, C -> 100, D -> 500, M -> 1000
<br>
Значение римской цифры не зависит от позиции, а знак минус - зависит

Проверить существует ли цифра! Важна последовательность цифр, XI = 11 / IX = 9, XV = 15 VX - не существует
<br>
Значение римских знаков `switch case`, case - свой символ + сравнение с предыдущим/последующим

Как вариант: https://gist.github.com/vocalinternet/aa2c67d1411b12483977ca3acda6039d
<br>
https://www.kalkulaator.ee/ru/konverter-rimskix-i-arabskix-chisel
<br>
http://graecolatini.bsu.by/htm-different/num-converter-roman.htm

https://www.google.com/search?q=convert+roman+numeral+to+integer+c%2B%2B

**Сложный вариант**
```c++
#include <iostream>
using namespace std;


int funSymbol(char symbol) {
	switch (symbol) {
	case 'I': return    1; break;
	case 'V': return    5; break;
	case 'X': return   10; break;
	case 'L': return   50; break;
	case 'C': return  100; break;
	case 'D': return  500; break;
	case 'M': return 1000; break;
	}
	return 0;
}


int main()
{
	string x = ""; // вводимое число
	cout << "x = ";
	cin >> x;
	
	for (int i = 0; i < x.size(); i++) // проверка всех line[i] на 0
		if (funSymbol(x[i]) == 0) {
			cout << "null";
			return 1;
		}
			
	int number = 0; // итоговое число-ответ
	int last = funSymbol(x[0]); // line[i-1] = начальный символ
	int counter = 1; // счётчик мест числа
	
	for (int i = 1; i < x.size(); i++) { // пробегание по всем символам line[i] строки
		if (counter > 2) {
			cout << "Incorrect number";
			return 2;
		}
		          
		int rimLine = funSymbol(x[i]); // символ line[i] в римской записи
		
		if (last == rimLine) // если line[i-1] = line[i]
			counter++;
	
		if (last < rimLine) // если меньшая цифра перед большей
			number -= (last * counter);

		if (last > rimLine) // если большая перед меньшей
			number += (last * counter);
			
		if (last != rimLine) // если line[i-1] не= line[i]
			counter = 1;
			
		last = rimLine; // line[i-1] становится line[i]
	}
	
	if (last == funSymbol(x[x.size() - 1])) {
		number += funSymbol(x[x.size() - 1]) * counter;
	}
	
	cout << "Number = " << number << endl;
	return 0;
}
```

**Лучший вариант**
```c++
#include <iostream>
using namespace std;


int digit(char x) { // римские числа в арабские
	switch(x) {
		case 'I': return 1;
		case 'V': return 5;
		case 'X': return 10;
		case 'L': return 50;
		case 'C': return 100;
		case 'D': return 500;
		case 'M': return 1000;
	}
	return -1;
}


int convert(string x) {
	int i;
	int j = 0;
	int lenX;
	int result = 0;
	lenX = x.length() - 1;
	
	for(i = lenX; i >= 0; i--) {
		if (digit(x[i]) >= j)
			result += digit(x[i]);
		else
			result -= digit(x[i]);
		j = digit(x[i]);
	}
	return result;
}

int main() {
  string x;
  cout << "Number = ";
  cin >> x;
  cout << convert(x) << endl;
  main();
}
```

### 4.7 «Генератор псевдослучайных чисел».
**Задание сделано слегка неправильно и сложно, надо делать рекурсией!**

Построить генератор псевдослучайных чисел по рекуррентной формуле:
s(i+1) = (m*s(i) + b) % c, где m, b, c – целые числа.
<br>
I вариант: m = 37, b = 3, c = 64
<br>
II вариант: m = 25173, b = 13849, c = 65537
<br>
Начальное значение s0=0

2 цикла для разных вариантов!

```c++
#include <iostream>
using namespace std;

int main()
{

	int m1 = 37;
	int b1 = 3;
	int c1 = 64;
	int m2 = 25173;
	int b2 = 13849;
	int c2 = 65537;
	int i; // ввод i
	int temp_i1 = 0; // временный i
	int temp_i2 = 0; // временный i
	cout << "i = ";
	cin >> i;
	int s1[i]; // создание ячеек для чисел 1 варианта
	int s2[i]; // создание ячеек для чисел 2 варианта
	s1[0] = 0;
	s2[0] = 0;
	
	while (temp_i1 != i + 1) {
		cout << temp_i1 << ") " << s1[temp_i1] << endl;
		s1[temp_i1 + 1] = (m1 * s1[temp_i1] + b1) % c1;	
		temp_i1 += 1;
	}
	cout << "--------\n";
	while (temp_i2 != i + 1) {
		cout << temp_i2 << ") " << s2[temp_i2] << endl;
		s2[temp_i2 + 1] = (m2 * s2[temp_i2] + b2) % c2;	
		temp_i2 += 1;
	}
	cout << "--------\n";
	cout << temp_i1 << ") " << s1[temp_i1] << endl;
	cout << temp_i2 << ") " << s2[temp_i2] << endl;
    return 0;
}
```

### 4.8 «Умножение матриц».
3 продавца продают 4 вида товаров.
<br>
Таблица А - количество продаваемого товара
<br>
Таблица B - цена каждого товара и комиссионные, полученные от продажи

![изображение](https://user-images.githubusercontent.com/70198995/193238312-c4deef88-a7cb-42de-a149-c9a67eda96a3.png)

Задать таблицы матрицы A и B, получить матрицу C = A * B и определить:
1) какой продавец выручил больше всего денег с продажи, какой – меньше
2) какой получил наибольшие комиссионные, какой – наименьшие
3) чему равна общая сумма денег, вырученных за проданные товары;
4) сколько всего комиссионных получили продавцы
5) чему равна общая сумма денег, прошедших через руки продавцов?

Комиссионые не включены в цену товара, вычитать их не нужно

```c++
#include <iostream>
using namespace std;

int main()
{
    double matrix_a[3][4] = { // 3x4
        {5, 2, 0, 10},
        {3, 5, 2, 5},
        {20, 0, 0, 0}};
                
    double matrix_b[4][2] = { // 4x2
        {1.20, 0.50},
        {2.80, 0.40},
        {5.00, 1.00},
        {2.00, 1.50}};
        
    double matrix_c[3][2]; // 3x2

    for (int x = 0; x < 3; x++) {
        for (int y = 0; y < 2; y++) {
            for (int i = 0; i < 4; i++) {
                matrix_c[x][y] += matrix_a[x][i] * matrix_b[i][y];
            }
        }
    }

    // Вывод матрицы C
    for (int x = 0; x < 3; x++) {
        for (int y = 0; y < 2; y++) {
            cout << matrix_c[x][y] << "               ";
        }
        cout << endl;
    }
    cout << "------------------------------\n";
    
	//////////////////////////////////////////////////////// Деньги
    int maxSeller = 0;
	int minSeller = 0;
    double maxMoney = 0;
	double minMoney = 10000000;
    for (int x = 0; x < 3; x++) {
        if (matrix_c[x][0] > maxMoney) {
			maxSeller = x + 1;
			maxMoney = matrix_c[x][0];
		}
        if (matrix_c[x][0] < minMoney) {
			minSeller = x + 1;
			minMoney = matrix_c[x][0]; 
		}
    }
    cout << "Seller " << maxSeller << " MaxMoney: " << maxMoney << endl;
    cout << "Seller " << minSeller << " MinMoney: " << minMoney << endl;
    
	//////////////////////////////////////////////////////// Комиссионные
    maxSeller = 0;
	minSeller = 0;
    double maxComss = 0;
	double minComss = 10000000;
    for (int x = 0; x < 3; x++) {
        if (matrix_c[x][1] > maxComss) {
			maxSeller = x + 1;
			maxComss = matrix_c[x][1]; 
		}
        if (matrix_c[x][1] < minComss) {
			minSeller = x + 1;
			minComss = matrix_c[x][1]; 
		}
    }
    cout << "Seller " << maxSeller << " MaxComss " << maxComss << endl;
    cout << "Seller " << minSeller << " MinComss " << minComss << endl;

	//////////////////////////////////////////////////////// Общая сумма денег
    double sumMoney = 0;
    for (int x = 0; x < 3; x++) {
    	sumMoney += matrix_c[x][0];
	}
    cout << "SumMoney = " << sumMoney << endl;
    
	/////////////////////////////////////////////////////// Общая сумма комиссионных
    double sumComss = 0;
    for (int x = 0; x < 3; x++) {
    	sumComss += matrix_c[x][1];
	}
    cout << "SumComss = " << sumComss << endl;

	/////////////////////////////////////////////////////// Общая сумма денег (+ комиссионные)
    double SumMoneyResult = 0;
    for (int x = 0; x < 3; x++) {
    	SumMoneyResult += matrix_c[x][0] + matrix_c[x][1];
	}
    cout << "SumMoneyResult = " << SumMoneyResult << endl;
}
```

### 4.9 «Системы счисления».
Программа должна считывать с клавиатуры число, записанное в одной системе счисления, и выводить на экран это число в записи по другому основанию
<br>
Исходное число – 112D, старое основание – 16, новое основание – 8, результат – 10455.

От 2 до 16 СС должно быть!

```c++
#include <iostream>
#include <string>
#include <cmath>
using namespace std;


int char_to_int(char symbol) {
	switch (symbol){
	case '0': return 0; break;
	case '1': return 1; break;
	case '2': return 2; break;
	case '3': return 3; break;
	case '4': return 4; break;
	case '5': return 5; break;
	case '6': return 6; break;
	case '7': return 7; break;
	case '8': return 8; break;
	case '9': return 9; break;
	case 'A': return 10; break;
	case 'B': return 11; break;
	case 'C': return 12; break;
	case 'D': return 13; break;
	case 'E': return 14; break;
	case 'F': return 15; break;
	}
	return -1;
}


string int_to_char(int symbol) {
	switch (symbol) {
	case 0: return "0"; break;
	case 1: return "1"; break;
	case 2: return "2"; break;
	case 3: return "3"; break;
	case 4: return "4"; break;
	case 5: return "5"; break;
	case 6: return "6"; break;
	case 7: return "7"; break;
	case 8: return "8"; break;
	case 9: return "9"; break;
	case 10: return "A"; break;
	case 11: return "B"; break;
	case 12: return "C"; break;
	case 13: return "D"; break;
	case 14: return "E"; break;
	case 15: return "F"; break;
	}
	return "";
}


double funTenCC(string line, int base_num = 2) { // перевод в 10 с.с.
	double new_x = 0; // полученное число в 10 с.с.
	
	for (int i = 0; i < line.size(); i++) { // пробегание по всем цифрам
		int symbol = char_to_int(line[i]); // конвертированный символ в цифру
		new_x += symbol * pow(base_num, line.size() - i - 1); // запись в число цифры line[i]
	}
	
	return new_x;
}


string funNewCC(int num, int base_num = 2) { // перевод в нужную с.с.
	string new_x = int_to_char(num % base_num);
	
	if (num > 0) {
		return funNewCC(num / base_num) + new_x; 
	}
	
	new_x = "";
	return new_x;
}


int main()
{
	string x;
	int old_ss, new_ss;
	cout << "Number: ";
	cin >> x;
	cout << "Old CC: ";
	cin >> old_ss;
	cout << "New CC: ";
	cin >> new_ss;
	
	int num = funTenCC(x, old_ss);
	cout << "Number: " << num << endl;
	cout << "Number: " << funNewCC(num, new_ss)  << endl;
    return 0;
}
```


## Домашнее задание 5

### 5.1 «Алгоритм Евклида» (слегка кривой вариант)
Задать 2 числа и найти их наибольший общий делитель 2 способами: делением и вычитанием.

Алгоритм поиска наибольшего общего делителя (НОД) двух чисел в 2 исполнениях (методом вычитания, остатка от деления).

2 целых положительных числа в пределах типа int: 30, 18 / Ответ 6

**Кривой вариант**

```c++
#include <iostream>
#include <cmath>
using namespace std;


int NODminus(int a, int b) {
    if (a == b)
		return a;
    if (a > b)
		return NODminus(a - b, b);
    if (a < b)
		return NODminus(a, b - a);
}

int NODdevision(int a, int b) {
    if (a > b)
		return NODdevision(a % b, b);
    if (a < b)
		return NODdevision(a, b % a);
}

int main() {
    double a, b;
    cout << "Enter a: ";
    cin >> a;
    cout << "Enter b: ";
    cin >> b;
    if (a <= 0 or b <= 0) {
        cout << "Error" << endl;
    }
    else {
	 	cout << "NODminus = " << NODminus(abs(a), abs(b)) << endl;
    	cout << "NODdevision = " << NODdevision(abs(a), abs(b)) << endl;
	}
}
```

**Более красивый вариант**

```c++
#include <iostream>
#include <cmath>
using namespace std;



int NODminus(int a, int b) {
    while (a > 0 and b > 0)
        if (a > b)
            a -= b;
        else
            b -= a;
    return a + b;
}

int NODdevision(int a, int b) {
    while (a > 0 and b > 0)
        if (a > b)
            a %= b;
        else
            b %= a;
    return a + b;
}


int main() {
    double a, b;
    cout << "Enter a: ";
    cin >> a;
    cout << "Enter b: ";
    cin >> b;
    if (a <= 0 or b <= 0) {
        cout << "Error" << endl;
    }
    else {
	 	cout << "NODminus = " << NODminus(abs(a), abs(b)) << endl;
    	cout << "NODdevision = " << NODdevision(abs(a), abs(b)) << endl;
	}
}
```

### 5.2 «Решето Эратосфена»
Найти все простые числа в диапазоне от 2 до введенного вами натурального числа

Ряд простых чисел от 2 до введённого числа: 25 / Ответ 3, 5, 7, 11, 13, 17, 19, 23

```c++
#include <iostream>
using namespace std;

int main() {
    int n; // заданное число
    cout << "n: ";
    cin >> n;
    int arr[n]; // массив
    for (int i = 0; i <= n; i++) { // счётчик i до n
    	if (i < 3) // если число < 3
    		arr[i] = 0; // удаляем число
    	else
    		arr[i] = i; // все остальные числа
	}

    for (int y = 0; y < n; y++) { // счётчик y до n
		if (arr[y] != 0) // если число не = 0
			for (int x = y; x < n; x++) // счётчик x до n
				if (arr[x] % arr[y] == 0 and arr[x] != arr[y]) // если остаток двух чисел = 0 и они не равны
					arr[x] = 0; // удаляем число
	} 
    for (int i = 0; i < n; i++) { // счётчик i до n                                     
		if (arr[i] != 0) // если число не = 0
			cout << arr[i] << endl;
	}
}
```

**Более простой вариант**

```c++
#include <iostream>
#include <cmath>
using namespace std;

bool checkSimple(int x) {
	for (int i = 2; i <= sqrt(x); i++) {
	    if (x % i == 0) {
	        return false;
	    }
	}
	return true;
}

int main() {
    int n;
    cout << "n: ";
    cin >> n;
    int arr[n];

	for (int i = 0; i < n; i++) {
	    arr[i] = i;
	}

    for (int i = 0; i < n; i++) {                                   
		if (checkSimple(arr[i]) == true)
			if (arr[i] != 0 and arr[i] != 1)
				cout << arr[i] << endl;
	}
}
```

Гайд по файлам: https://ejudge.179.ru/tasks/cpp/total/161.html

### 5.3 «Обработка текстовых файлов» (2 варианта)

1. Замена пробелов на что-то https://pastebin.com/br3t26b2


```c++
// 15. Поиск определенного слова в текстовом файле
#include <stdio.h>
#include <conio.h>
#include <string>
#include <iostream>
#include <fstream>
using namespace std;
 
int main() {
    ifstream ifile("53.txt");
    string word = "";
    string result = "";
    char letter = ' ';
    
    cout << "Enter a word: ";
	cin >> word;
 
    while (ifile.peek() >= 0) { // проход до конца файла
        ifile >> letter;
		result += letter;
    }
    ifile.close();

    int pos = result.find(word, 0);
    
    if (pos != -1) {
		cout << "Position word: " << pos << endl;
	}
    else {
    	cout << "word not found...\n";
	}

    return 0;
}
```
**Не работает с файлами**
```c++
// 5. Поиск в тексте фразы максимальной длины
#include <iostream>
using namespace std;

int main() {
	string str, w, strLen, d = " ";
	cout << "string: = ";
	getline(cin, str);
	int b, e = 0;
	while ((b = str.find_first_not_of(d, e)) != str.npos) {
		e = str.find_first_of(d, b);
		w = str.substr(b, e - b);
		if (w.size() > strLen.size())
			strLen = w;
	}
	cout << strLen << endl;
	cout << "-----------------------------------------\n";
	main();
}
```

```c++
// 5. Поиск в тексте фразы максимальной длины
#include <iostream>
#include <fstream>
using namespace std;

int main() {
	ifstream ifile("53.txt");
	string str, w, strLen, d = " ";
	string letter = "";
	 while (ifile.peek() >= 0) { // проход до конца файла
        ifile >> letter;
		str = str + letter + " ";
    }
    ifile.close();
    
	int b, e = 0;
	while ((b = str.find_first_not_of(d, e)) != str.npos) {
		e = str.find_first_of(d, b);
		w = str.substr(b, e - b);
		if (w.size() > strLen.size())
			strLen = w;
	}
	cout << strLen << endl;
	return 0;
}
```

```c++
// Поиск длины фразы (немного не то задание)
#include <iostream>
#include <fstream>
#include <cstring>
using namespace std;
 
int main()
{
    int max = 0, lenStr, count = 0;
    string line;
    ifstream ifile("53.txt");
    	
    char str[1024];
    ifile.getline(str, 1024);
    
    for (int i = 0; i < strlen(str); i++) {
         lenStr = 0;
         for (int j = i; str[ j ] != ' ' and str[ j ] != '\0'; j++ ) {
		 	lenStr++;
         	if (lenStr > max)
				max = lenStr;         	
		 }
    }
    
    
    cout << max << endl;
}
```

### 5.4 «Ряды»

```c++
// 12. Дано натуральное число n. Вычислить
#include <iostream>
#include <cmath>
using namespace std;

double summN(int n, double k = 1, double low = 0) {
    double fact = 1;
    for (int i = 1; i <= k; i++)
		fact = fact * i; // Факториал
		
    low += (1 / k); // сумма дробей
    double result = fact / pow(low, k);
    if (n == k)
		return result;
    return summN(n, ++k, low) + result;
}

int main() {
    setlocale(0, "");
    int n;
    cout << "Enter n: ";
    cin >> n;
    cout << "y = " << summN(n) << endl; // сумма всех n
    return 0;
}
```

```c++
// 13. Дано натуральное число m < 27. Получить все трехзначные целые числа, сумма цифр которых равна m (использовать полный перебор)
#include <iostream>
using namespace std;
 
int digitsSum(int n) {
  int sum = 0;
  while (n != 0) {
    sum += n % 10;
    n /= 10;
  }
  return sum;
}

int main() {
	int m;
    cout << "m = ";
    cin >> m;	
	for (int i = 100; i <= 999; i++) {
		if (digitsSum(i) == m) {
			cout << i << endl;
		}
	}
}
```

### 5.5 «Файлы»
```c++
// 25. Организовать создание текстового файла. Подсчитать в текстовом файле число непустых строк, в которых символы упорядочены по возрастанию.
#include <iostream>
#include <fstream>
#include <string>
#include <algorithm>

using namespace std;

int main () {
  string strX = "";
  
  ofstream file("55.txt");
  while (strX != "0") { // ввод чисел
  	cout << "Input string: ";
  	getline(cin, strX);
 	file << strX << "\n"; // запись в файл
  }
  file.close();
  
  int k = 0;
  ifstream ifile("55.txt"); // создать текстовый файл
  string str;
  while (getline(ifile, str)) {
    if (is_sorted(str.begin(), str.end())) k++;
  }
  ifile.close();
  
  cout << "result: "<< k - 1;
  return 0;
}
```

