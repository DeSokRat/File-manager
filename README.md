from os import remove
from os import rename
from os import chdir
def delete_file(name_file: str) ->None:
    try:
        remove(name_file)
    except:
        print(f'[ERROR] Файл "{name_file}" не найден! ')
    else:
        print(f'[INFO] Файл был успешно удалён! ')

def rename_file(old_name, new_name: str) :
    try:
        rename(old_name, new_name)
    except:
        print(f'[ERROR] Файл не найден! ')
    else:
        print(f'[INFO] Файл успешно переименован! ')

def change_file(name_file: str):
    
    try:
        chdir(name_file)
    except:
        print(f'[ERROR] Файл не найден: ')
        
        
        
        fff
        
from deF import rename_file
from deF import delete_file
from deF import change_file
print('Добро пожаловать в "Файловый менеджер!":\n ')

print('Список доступных команд: \n/create\n/delete\n/change\n/rename\n/exit')

print()

while True:
    command = input('Введите команду: ')
    if command ==  '/rename':
       old_name = input('Введите старое название файла: ')
       new_name = input('Введите новое название файла: ')
       rename_file(old_name, new_name)
    
    elif command == '/create':
        name_file = input('Введите название файла: ')
        format_file = input('Введите формат файла: ')
        with  open(name_file,'x') as f:
         print(f'[INFO] Файл "{name_file}" успешно создан!')
            
   
    
    elif command == '/delete':
        name = input('Введите название файла: ')
        delete_file(name)
    
  

    elif command == '/change':
        name_file = input('Введите название файла: ')
        print('1) Записать данные в файл\n2) Перезаписать данные в файле\n3) Удалить данные с файла')
        command = input('Ваш выбор: ')
        if command ==1:
           with open ("name_file.txt", "a") as f:
                name_file
        if command ==2:
           with open("name_file.txt", "w") as f:
                name_file
        if command == 3:
           with open("name_file.txt", "w") as f:
          
               change_file("name_file", "txt", "w")
