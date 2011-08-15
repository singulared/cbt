Readme:

@todo:
Всю инициализацию необходимо производить после загрузки всех фреймов.
По таймауту, либо как более лучший вариант смотреть статус главного фрейма (top.frames[main_uid])

@todo:
Список фреймов - top.frames[]
Правда неизвестно, можно ли через них манипулировать контентом.

todo list:

all:
+\-	get context state
dungeon:
+		get coordinates 
+		get path
-		use objects
-		attack on bots
-		walk
battle:
-		submit turn
-		tactics use
	


========================== Чат ==========================

Пишем в чат:
1) добавляем в поле:
$(top.frames[10].document.body).find('#T2 input').val('test\n\r')
2) отправляем
$(top.frames[10].document.body).find('#F1').submit();

Добавить html в лог чата:
top.Chat.am('html')

Добавляем вкладку:
top.Chat.Self.arrTabs['cbt'] = top.Chat.Self.oTab.AddTab('1','cbt','1') //не знаю зачем 1 и 3 параметры
top.Chat.Self.arrTabs['cbt'].Show()

Помечаем цветом вкладку
top.Chat.Self.arrTabs['chat'].Mark()

Чат object top.Chat
Методы:
	Clear() - Очистка
	am(text) - добавить в лог чата
	sml(smile) - добавить смайлик smile['code'] = 'susel'
	self:
		AddLogs(a)
		AddMessage(r) - Раскрашенные сообщения
		ArrLogs
		ArrTabs
		CtxMenu() - КОнтекстное меню
		CtxMenuHide()
		oTabs:
			Методы...

========================== Бой ==========================

Кнопка хода: $('.UserBattleCommit').click();
Автоудары:
	function fight()
	{
		$('.UserBattleCommit').click();
		setTimeout(function() {fight()} , 2000);
	}


frames['batle'] - Лог боя
	
======================== Пещеры =========================

Карта перемещений
main_uid - имя главного фрейма
$(top.frames['main283318524'].document.body).find('#MoveMap').html() 

$(top.frames[main_uid].document.body).find('script')[8].text
$(top.frames[main_uid].document.body).find('script')[10].text
Скрипты построения карты.

$(top.frames[main_uid].document.body).find('#MoveMap area') - Список элементов для click $(top.frames[main_uid].document.body).find('#MoveMap area')[0].click()
Остается только распарсить возможные варианты перемещения.

------
нападения и действия.
1) Сначала получаем список Area c активными на этой клетке элементами ($(top.frames[main_uid].document.body).find('area')) стоит отметить что не все они активные,
так же тут есть просто расположенные в пределах видимости.
Кликаем
$(top.frames[main_uid].document.body).find('area')[0].click()
2) Если действий с элементом несколько, (действие идет через меню. (Боты, нападения)) Ищем появившиеся жлементы меню.
$(top.frames[main_uid].document.body).find('a') Такого типа:
"<A onclick="return p_action('attack=1&amp;use','1.4.2.194-7')" href="http://sandcity.combats.com/dungeon2.pl?rnd=0.65379233024434&amp;path=m1#">Напасть</A>" 
Кликаем.
>> $(top.frames[main_uid].document.body).find('a')[2].click() 

------
Подбор предметов.
Все выпавшие предметы
$(top.frames[main_uid].document.body).find('a')[2] (Начиная со второго)
$(top.frames[main_uid].document.body).find('a')[2].click() - Подбор