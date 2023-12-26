#Создание локального репозитория и синхронизация с удаленным
----

1. Создаете аккаунт на Github.com

2. Переходите в папку с проектом через консоль с помошью команды cd в Git.

3. Инициализируете репозиторий с помощью команды git init.

4. На Github.com заходите в свой профиль, нажимаете на вкладку Repositories, нажимаете New, называете удаленный репозиторий, нажимаете Create repository.

5. Создает SSH-ключи. Убедиться, что их еще нет: 
  ```- cd ~
  - ls -la .ssh/
```

6. Если нет, то создаем: 
  - ssh-key-keygen -t ed25519 -C "электронная почта, с которой регестрировались на гитхаб"

7. Проверить, что ключи сгенерировались: ls -a ~/.ssh

8. Копируем содержимое файла с публичным ключем в буфер обмена:  ```$ clip < ~/.ssh/id_ed25519.pub
```

9. Перейдите на GitHub и выберите пункт Settings в аккаунте.

10. В меню нажмите на пункт SSH and GPG keys.

11. Выберите New SSH key.

12. В поле Title напишите название ключа.

13. В поле Key скопируйте ваш ключ из буфера обмена.

14. Нажмите на кнопку Add SSH key (англ. «добавить SSH-ключ»).

15. Проверьте правильность ключа с помощью команды:  ```$ ssh -T git@github.com
```

16. Перейдите на страницу удалённого репозитория, выберите тип SSH и скопируйте URL.

17. Введите в консоль 

```$ cd ~/dev/first-project

$ git remote add origin (Вставьте ссылку, без скобочек)
```

18. Локальный репозиторий и удаленный связаны! 

19. Проверить успех операции можно с помощь команды: ``` $ git remote -v
```
 