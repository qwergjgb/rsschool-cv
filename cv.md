## Стукалова Дана Андреевна

**Контакты:**

* **Электронная почта:** stukalovadana20@gmail.com
* **Телефон:** +375292710932
* **Discord:** ghost
* **GitHub:** https://github.com/qwergjgb

**О себе:**

Я - студентка 2 курса Витебского государственного технического университета, факультета информационных технологий и робототехники, специальности “Информационные технологии”. Я увлечена разработкой веб-приложений и стремлюсь развиваться в сфере front-end разработки. В своей работе я ценю аккуратность, эффективность, командную работу, и считаю, что способность быстро учиться и адаптироваться к новым технологиям - одно из моих главных преимуществ.

**Навыки:**

* **Языки программирования:** C++, C#, JavaScript, HTML, CSS
* **Инструменты разработки:** Visual Studio, Visual Studio Code, CodeBlocks, Git, IntelliJ IDEA

**Пример кода:** 
* **Игра "Камень Ножницы Бумага Ящерица Спок"**
  
  ```cpp
  #include <iostream>
#include <Windows.h>
#include <string>
#include <ctime>

using namespace std;

string getSHELDONChoice() {
    string choices[] = { "камень", "ножницы", "бумага", "ящерица", "спок" };
    int randomIndex = rand() % 5;
    return choices[randomIndex];
}

string whoWinner(string youChoice, string sheldonChoice) {
    // Определение победителя
    string winnerDict[5][2] = {
      {"ножницы", "ящерица"}, // Камень побеждает Ножницы и Ящерицу
      {"бумага", "спок"},     // Ножницы побеждают Бумагу и Спока
      {"камень", "ящерица"},  // Бумага побеждает Камень и Ящерицу
      {"спок", "бумага"},     // Ящерица побеждает Спока и Бумагу
      {"камень", "ножницы"}   // Спок побеждает Камень и Ножницы
    };

    // Проверка на ничью
    if (youChoice == sheldonChoice) {
        return "Ничья!\n-ДАВАЙ ЕЩЕ РАЗ!!!!!!!!!";
    }

    // Проверка на победу игрока
    for (int i = 0; i < 2; ++i) {
        if (winnerDict[youChoice[0] - 'а'][i] == sheldonChoice) {
            return "Вы победили!\n-ТАК НЕЧЕСТНО ДАВАЙ ЕЩЕ РАЗ Я ВСЕ РАВНО ТЕБЯ ПОБЕДЮ!!!!!";
        }
    }

    return "Шелдон победил!\n-БУГАГАШЕНЬКИ! ХА-ХА";
}

void playRound(string youChoice) {
    string sheldonChoice = getSHELDONChoice();
    string winner = whoWinner(youChoice, sheldonChoice);
    cout << "Вы выбрали: " << youChoice << endl;
    cout << "Шелдон выбрал: " << sheldonChoice << endl;
    cout << winner << endl;
}

int main() {
    SetConsoleCP(1251);
    SetConsoleOutputCP(1251);
    // Инициализация генератора случайных чисел
    srand(time(0));

    string youChoice;
    cout << "Введите свой выбор (камень, ножницы, бумага, ящерица, спок): ";
    cin >> youChoice;
    playRound(youChoice);

    return 0;
}
```

**Опыт:**

* **[Название проекта]**: “Разработка простого веб-сайта на HTML, CSS и JavaScript”.

**Образование:**

* **Витебский государственный технический университет**: Информационные технологии (2023 - настоящее время)

**Английский язык:**

* **Уровень:** Средний
* **Опыт:** Активное использование в работе и учебе.

**Проект: “CV”**:

* **Описание:** Это моё CV, которое я разработала, используя Markdown.
* **Ссылка на код:** https://github.com/qwergjgb/rsschool-cv.git
