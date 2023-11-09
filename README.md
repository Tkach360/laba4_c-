# laba4_c-
Статические поля:
Double Credit::maxCreditAmout – максимальная сумма кредита, который может считаться “хорошим”.
Int Account::nextUniqueID – для присвоения каждому объекту Account уникального ID.

Статические методы:
	double Credit::getRegularContribution() – возвращает размер регулярных выплат по кредиту исходя из тела кредита, процента и срока.
	void Credit::setMaxCreditAmout() – установка maxCreditAmout.
	Double Credit::getMaxCreditAmout() – получение maxCreditAmout.
	bool Credit::checkCredit() – для проверки кредита на наличие ошибок (true если кредит “хороший” и false в противном случае) имеет 2 перегрузки: для параметров кредита и самого кредита.

В проекте на C++:

1)	Возвращение значений через ссылку:
vector<Account>& Client::getAllAccounts()
vector<Deposit>& Client::getAllDeposits()
vector<Credit>& Client::getAllCredits()

2)	Возвращение значений через указатель:
Account* Client::getAccountByID(int searchID)


3)	Использование оператора this в методе Client::addNewAccount(); (каждый объект класса Account имеет ссылку на объект класса Client)

4)	Дружественные функции для Client:
friend void BankService::setYear(int newYear);
	friend void BankService::setBody(double newBody);
	friend void BankService::setPercent(double newPercent);
	friend void Credit::setContrib(double newContrib);

5)	Перегрузки операторов:
Перегружены операторы + и ++ (префиксная и постфиксная формы)
Все функции вывода данных об объекте класса заменены на перегрузки оператора <<
6)	Все данные char заменены на std::string
