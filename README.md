прежде всего скачиваем папку со всеми нужными программами [ссылка на Drive](https://drive.google.com/drive/folders/1aGdnFz87eYeD-STuirSgTE9M0wwGeQUD?usp=drive_link)

если нужно настроить принтер с нуля начинать с п. 1, если подключится к уже существующему принтеру, начинать с п. 14
1. подключаем принтер по USB
2. открываем Diagnostic Tool
3. нажимаем **Setup**(1.1), проверяем что он увидел принтер, и жмем **Get Status**(1.2)
4. нажимаем **Get**(1.3), чтобы программа смогла считать уже установленные данные
![Screenshot 2025-01-15 182445](https://github.com/user-attachments/assets/7b32f413-4a37-465e-8bb3-894edfa68f7e)
5. дальше переходим во вкладку **BT/WIFI** (у меня подключен принтер без WiFi, все поля должны автоматически заполнится)
6. обязательно выключаем DHSP и выставляем свободный локальный IP(2.1)
7. нажимаем **Set**(2.2), чтобы применить
![Pasted image 20250115183446](https://github.com/user-attachments/assets/e678d591-5efa-4e46-ac38-482aa90a1526)
8. далее нажимаем **Scan**(3.1), чтобы найти все доступные сети WiFi
9. выбираем нужную и вписываем пароль в поле PIN(3.2)
10. нажимаем **Conn**(3.3), чтобы подключится, обратите внимание, что поле IP(3.4) должно поменяться на тот что вы установили перед этим
   *если этого не произошло, проверьте что в блоке WiFi STA DHCP, все стоит верно в соответствии с п. 6, и то что вы после этого нажали Set, после повторите п. 10*
11. дальше нажимаем Set(3.5) и Save(3.6)
![Pasted image 20250115184349](https://github.com/user-attachments/assets/38cabb36-da7e-4cb3-a7e3-5b2722233844)
12. c Diagnostic Tool мы закончили, теперь переходим к настройке драйвера на ПК
13. включаем DriverWizard(в папке Seagull)
14. Установить драйверы принтера
	1. возможно нужно будет удалить драйвера для проводных подключений, если они у вас сейчас не подключены(принтеров имеется ввиду), потому что установщик не позволяет не обновлять драйвера
	2. это делается через “Удалить драйверы принтера”
15. Сеть (Ethernet или WiFi)
16. выбираем принтер(в данный момент мы работаем с Xprinter XP-420B)
17. и самое интересное создание порта
![Pasted image 20250115185519](https://github.com/user-attachments/assets/a38975ad-ecce-4dc4-a6a8-287d37a046bd)
18. выбираем Standart TCP/IP Port
![Pasted image 20250115185544](https://github.com/user-attachments/assets/42a056ce-0f14-4039-bc2f-ea93c664588a)
19. тут выставляем локальный IP принтера, который вы поставили в Diagnostic Tool
    имя порта можно поставить любое, поэтому лучше назвать его как-нибудь понятно
    ![Pasted image 20250115185749](https://github.com/user-attachments/assets/f3f19c4a-7e36-4c3f-91e5-a3e156c4e2dd)
20. дальше он долго будет искать, но так и ничего не найдет, нас это устраивает
21. после долгих поисков он предложит настроить вручную, выбираем Xprinter или Brother любой
![Pasted image 20250115185953](https://github.com/user-attachments/assets/23b30405-d76d-4232-b96c-1a8dce135acb)
22. теперь порт появится в выборе
![Pasted image 20250115190048](https://github.com/user-attachments/assets/12a33054-5d31-4191-a913-9bf0fcf0ad31)
23. установщик предложит поменять номер порта, соглашаемся
24. дальше выставляем имя самого принтера, общий доступ нам не нужен![Pasted image 20250115190217](https://github.com/user-attachments/assets/f627dbd2-50be-48df-a4dc-e19d8b4e6941)

25. далее обязательно нужно проверить что порт настроился правильно
26. заходим в настройки-принтеры ищем тот который только что настраивали “Управление” - “Свойства принтера”
27. тут переходим во вкладку “Порты” и жмем “Настроить порт…”
28. меняем протокол с LPR на Raw
![image](https://github.com/user-attachments/assets/2736f66a-540a-4a66-9983-3964502906f7)
29. жмем Ок - Применить, все закрываем и проверяем работу

вся документация, по которой учился я, так же есть в форматах PDF
