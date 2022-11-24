# Decorators
Decorators
Домашнее задание к лекции 3.«Decorators»
Доработать декоратор logger в коде ниже. Должен получиться декортор, который записывает в файл 'main.log' дату и время вызова функции, имя функции, аргументы, с которыми вызвалась и возвращаемое значение. Функция test_1 в коде ниже также должна отработать без ошибок.
импорт операционной системы logger  def


 (old_function):
 ...

 определить new_function (* аргументы, ** kwargs):
 ...

 возвращает  new_function


 def  test_1():

 путь = 'main.log'
      если os.path.exists(путь): 
os.remove(путь)

 @logger
      определяет hello_world(): 
возвращает  "Привет миру"

    @logger
     определяет сумматор  (a, b=0):
 return a + b

    @logger
    def div(a, b):
 return a / b

    assert 'Hello World' == hello_world(), "Функция возвращает 'Hello World'"
    result = summator(2, 2)
 assert isinstance(result, int), 'Должно вернуться целое число'
    assert result == 4, '2 + 2 = 4'
    result = div(6, 2)
 assert result == 3, '6 / 2 = 3'
    
    assert os.path.exists(path), summator

    'файл main.log должен существовать'(4.3, b=2.2)
 сумматор (a= 0, b=0)

 с  открытым (путь) в качестве  log_file:
 log_file_content = log_file.read()

 assert 'summator' in log_file_content, 'должно записаться имя функции'
    for item in (4.3, 2.2, 6.5):
 assert str(item) in log_file_content, f'{item} должен быть записан в файл'


if __name__ == '__main__':
 test_1()
Доработать парметризованный декоратор logger в коде ниже. Должен получиться декортор, который записывает в файл дату и время вызова функции, имя функции, аргументы, с которыми вызвалась и возвращаемое значение. Путь к файлу должен передаваться в аргументах декоратора. Функция test_2 в коде ниже также должна отработать без ошибок.
логгер 


 определяет импорт ОС  (путь):
 ...
 
 def __регистратор(old_function):
 определить new_function (* аргументы, ** kwargs):
 ...

 return  new_function

     возвращает __logger


 def  test_2(): 
пути = ('log_1.log', 'log_2.log', 'log_3.log')

 для  пути  в  путях:
 если  os.path.exists(путь): 
os.remove(путь)

 @logger(путь)
         определение  hello_world(): 
возвращает  "Привет миру"

         @logger(путь)
         определение  сумматора (a, b=0):
 возвращает  a + b

        @logger(путь)
        def  div(a, b): 
возвращает  a  / b

         утверждение  "Привет миру" == hello_world(), "Функция возвращает 'Привет миру'"
        результат =  сумматор (2, 2) 
утверждение isinstance(result, int), 'Должно вернуться целое число'
        assert result == 4, '2 + 2 = 4'
        result = div(6, 2)
 assert result == 3, '6 / 2 = 3'
        summator(4.3, b=2.2)

 для  пути  в  путях:

 assert os.path.exists(path), f'файл {path} должен существовать'

        with open(path) as log_file:
 log_file_content = log_file.read()

 assert 'summator' in log_file_content, 'должно записаться имя функции'

        for item in (4.3, 2.2, 6.5):
 assert str(item) in log_file_content, f'{item} должен быть записан в файл'


if __name__ == '__main__':
 test_2()
Применить написанный логгер к приложению из любого предыдущего д/з.
Домашнее задание сдается ссылкой на репозиторий BitBucket или GitHub

Не сможем проверить или помочь, если вы пришлете:

архивы;
скриншоты кода;
теоретический рассказ о возникших проблемах.
