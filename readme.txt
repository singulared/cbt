Readme:

@todo:
��� ������������� ���������� ����������� ����� �������� ���� �������.
�� ��������, ���� ��� ����� ������ ������� �������� ������ �������� ������ (top.frames[main_uid])

@todo:
������ ������� - top.frames[]
������ ����������, ����� �� ����� ��� �������������� ���������.

========================== ��� ==========================

����� � ���:
1) ��������� � ����:
$(top.frames[10].document.body).find('#T2 input').val('test\n\r')
2) ����������
$(top.frames[10].document.body).find('#F1').submit();

�������� html � ��� ����:
top.Chat.am('html')

��������� �������:
top.Chat.Self.arrTabs['cbt'] = top.Chat.Self.oTab.AddTab('1','cbt','1') //�� ���� ����� 1 � 3 ���������
top.Chat.Self.arrTabs['cbt'].Show()

�������� ������ �������
top.Chat.Self.arrTabs['chat'].Mark()

��� object top.Chat
������:
	Clear() - �������
	am(text) - �������� � ��� ����
	sml(smile) - �������� ������� smile['code'] = 'susel'
	self:
		AddLogs(a)
		AddMessage(r) - ������������ ���������
		ArrLogs
		ArrTabs
		CtxMenu() - ����������� ����
		CtxMenuHide()
		oTabs:
			������...

========================== ��� ==========================

������ ����: $('.UserBattleCommit').click();
���������:
	function fight()
	{
		$('.UserBattleCommit').click();
		setTimeout(function() {fight()} , 2000);
	}


frames['batle'] - ��� ���
	
======================== ������ =========================

����� �����������
main_uid - ��� �������� ������
$(top.frames['main283318524'].document.body).find('#MoveMap').html() 

$(top.frames[main_uid].document.body).find('script')[8].text
$(top.frames[main_uid].document.body).find('script')[10].text
������� ���������� �����.

$(top.frames[main_uid].document.body).find('#MoveMap area') - ������ ��������� ��� click $(top.frames[main_uid].document.body).find('#MoveMap area')[0].click()
�������� ������ ���������� ��������� �������� �����������.

------
������� � ��������.
1) ������� �������� ������ Area c ��������� �� ���� ������ ���������� ($(top.frames[main_uid].document.body).find('area')) ����� �������� ��� �� ��� ��� ��������,
��� �� ��� ���� ������ ������������� � �������� ���������.
�������
$(top.frames[main_uid].document.body).find('area')[0].click()
2) ���� �������� � ��������� ���������, (�������� ���� ����� ����. (����, ���������)) ���� ����������� �������� ����.
$(top.frames[main_uid].document.body).find('a') ������ ����:
"<A onclick="return p_action('attack=1&amp;use','1.4.2.194-7')" href="http://sandcity.combats.com/dungeon2.pl?rnd=0.65379233024434&amp;path=m1#">�������</A>" 
�������.
>> $(top.frames[main_uid].document.body).find('a')[2].click() 

------
������ ���������.
��� �������� ��������
$(top.frames[main_uid].document.body).find('a')[2] (������� �� �������)
$(top.frames[main_uid].document.body).find('a')[2].click() - ������