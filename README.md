# Anime Quiz

## flow (rus):
1. На стороне сервера создаётся "комната", к которой могут подключаться юзеры
2. У каждого юзера есть ws-коннект с сервером и стейт(ы)
3. Как только все юзеры будут готовы, то начинается игра
4. С сервера приходит ссылка на Ютуб-ролик, ролик запускается и у юзеров открывается юзер-инпут для ответа
5. п.4 повторяется, пока не закончатся ролики / админ комнаты не закончит игру
6. Показывается таблица лидеров и что-то ещё (кнопки шера результата в соц.сети)


# room
struct:
field - id
field — userConnections - map
field - roomState
field - currentQuiz
field - allQuizzes
field - adminID
method - handleUserAction


# roomRouter
struct:
field - rooms map[hash]*room
method - getRoomByHash()

// test youtube video = https://www.youtube.com/embed/gAjR4_CbPpQ?autoplay=1