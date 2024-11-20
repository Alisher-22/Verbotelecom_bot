from telegram import Update
from telegram.ext import Application, CommandHandler, MessageHandler, filters, CallbackContext

# Функция для обработки команды /start
async def start(update: Update, context: CallbackContext) -> None:
    await update.message.reply_text("Привет! Я твой бот.")

# Функция для обработки текстовых сообщений
async def echo(update: Update, context: CallbackContext) -> None:
    await update.message.reply_text(update.message.text)

# Основная функция, которая запускает бота
def main() -> None:
    # Создание объекта Application с вашим токеном
    application = Application.builder().token("7909237738:AAHJYLIEg-ay936TcUa4rQQKumpqCRL-u84").build()

    # Регистрируем обработчики команд
    application.add_handler(CommandHandler("start", start))

    # Регистрируем обработчик для текстовых сообщений
    application.add_handler(MessageHandler(filters.TEXT & ~filters.COMMAND, echo))

    # Запуск бота
    application.run_polling()

if __name__ == '__main__':
    main()
