# Class-PET-modificated-

from datetime import datetime

class Pet:
    def __init__(self, name='КТОТО', age=0, voice='АХТУНГ'):
        self.name = name
        self.age = age
        self.voice = voice

  def say(self):
      print(f'{self.name} каже: {self.voice}')

    # Метод для отримання року народження
  def get_birthday_year(self):
      current_year = datetime.now().year
      return current_year - self.age


# Дочірній клас для песика (собаки)
class Dog(Pet):
    def __init__(self, name='Песик', age=0, voice='Гав', breed='Невідома порода'):
        super().__init__(name, age, voice)
        self.breed = breed

  def about(self):
      print(f'{self.name} - порода: {self.breed}, вік: {self.age} років')

# Створюємо екземпляр класу Dog
my_dog = Dog(name='Рекс', age=3, voice='Гав-гав', breed='Німецька вівчарка')

# Викликаємо методи
my_dog.say()  # Виведе голос песика
my_dog.about()  # Інформація про песика
print(f'Рік народження: {my_dog.get_birthday_year()}')  # Виведе рік народження
