# telebot
Quando o bot for adicionado em algum grupo telebot 


```
#quando o meu bot for adicionando em algum grupo 
@bot.my_chat_member_handler()
def my_chat_m(message: types.ChatMemberUpdated):
    new = message.new_chat_member
    if new.status == "member":
        p = bot.send_message(message.chat.id,"obrigado por me adicionar \nno seu grupo , vou estar gerenciando o seu grupo para as boas-vindas , \nessas são as minhas boas vindas e as perguntas ⬇️ ") # ele vai iniciar essa mensagem
        #bot.leave_chat(message.chat.id)
        sleep(10)
        bot.delete_message(message.chat.id , p.id)
        return False

```
