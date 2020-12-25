# bot-sts
from pyrogram import Client, Filters

# التوكن الذي حصلت عليه من @botfather
# مثال :
# app = Client("bot", bot_token="1234567:ABCDEFGLLLL44GNVCCC")
app = Client("اسم الجلسة", bot_token="التوكن")

# اذا كانت الرسالة في الخاص و كانت الرسالة الامر /start
@app.on_message(Filters.private & Filters.command('start'))
def startmsg(client, message):
    # البوت سيقوم بالرد عليك بهذه الرسالة
  message.reply("اهلا بك في بوت همسات")

app.run() # لتشغيل البوت "long-polling"
