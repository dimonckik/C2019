from random import choice
class Randomaizer:
    def __init__(self, a, b):
        self.__a = a
        self.__b = b

    def __get_resultat(self):
        oper = ["+", "-", "*", "/"]
        operands = choice(oper)
        if operands == "+":
            return self.__a + self.__b
        if operands == "-":
            return self.__a - self.__b
        if operands == "*":
            return self.__a * self.__b
        if operands == "/":
            return self.__a / self.__b
    def result(self):
        return self.__get_resultat()
    def __str__(self):
        return self.__get_resultat()


my_random = Randomaizer(2, 9)
print(my_random.result())
print(my_random.__str__())
