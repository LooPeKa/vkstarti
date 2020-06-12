# Установка
```python
pip install vkstarti
```
# Установка обновления 
```python 
pip install vkstarti --upgrade
```
**2 раза**
# Простой бот на vkstarti
```python
import vkstarti
from vkstarti import Bot,Event

bot = Bot( "ТОКЕН" )

@vkstarti.potok
def kommand( event ):
	myevent = Event( event )
	if myevent.message("Ты",lower=True):
		bot.sms("Я")

while True:
	kommand( bot.on(  ) )
```
# sms
Отправляет сообщение

```message - Сообщение```
```id - ID пользователя которому придет сообщение ( По умолчанию event.user_id )```
```python
bot.sms( "Работай , Паша!", 1 )
```
# friendsadd
Кидает заявку в друзья 
```peer_id - ID пользователя которым придет заявка```
```text - Сообщение с которым поступит заявка в друзья```
```python
bot.friendsadd( 1, "Прими в друзья" )
```
# stick
Отправляет стикер 
```stick_id - ID стикера```
```id - Кому придет стикер ( По умолчанию event.user_id )```
```python
bot.stick( 1, 1 )
```
# sms_pin
Прикрепляет сообщение в беседе
```peer_id - ID чата```
```message_id - ID сообщения```
```python 
bot.sms_pin( 1, 2007 )
```
# sms_unpin
Открепляет сообщение в беседе
```peer_id - ID чата```
```python 
bot.sms_unpin( 1 )
```
# sms_editChat
Редактирует беседу 
```title - Новое название беседы```
```chat_id - ID чата ( По умолчанию event.chat_id )```
```python
bot.sms_editChat( "Программисты", 1 )
```
# sms_delete
Удаляет сообщение
```id - ID сообщения```
```from_all - Удалить для всех ( По умолчанию 0, 1 - для всех 0 - для себя )```
```python
bot.sms_delete( 228, 1 )
```
# sms_edit
Редактирует сообщение
```text - Новый текст сообщения ```
```peer_id - ID диалога ( По умолчанию event.peer_id )```
```sms_id``` - ID сообщения ( По умолчанию event.message_id )```
```python
bot.sms_edit( "ha" )
```
# sms_ban
Исключает участника беседы
```chat_id - ID беседы ( По умолчанию event.chat_id )```
```member_id - ID пользователя которого надо исключить ( По умолчанию event.member_id )```
```python
bot.sms_ban( 1, 1 )
```
# acc_ban
Кидает в Черный Список
```id - Перечисленные через запятую ID пользователей которых необходимо кинуть в ЧС```
```python
bot.acc_ban( 1, 228, 999, 777, 666, 333 )
```
# acc_unban
Убирает из Черного Списка
```id - Перечисленные через запятую ID пользователей которых необходимо убрать из ЧС```
```python
bot.acc_unban( 1, 228, 999, 777, 666, 333 )
```
# red
```python
text = "казино 1000"
vkstarti.red( "казино ", text )
```
Ответ >
```python
1000
```
