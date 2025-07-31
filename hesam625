# signal
from telegram import Update
from telegram.ext import Updater, CommandHandler, CallbackContext

# 🔑 توکن ربات تلگرامت رو اینجا بذار
TOKEN = "YOUR_BOT_TOKEN_HERE"

# 🟢 تابع شروع
def start(update: Update, context: CallbackContext):
    update.message.reply_text(
        "سلام! 👋\n"
        "من ربات سیگنال‌دهی هستم.\n"
        "برای دریافت سیگنال‌ها از دستور /signal استفاده کن."
    )

# 📊 تابع سیگنال
def signal(update: Update, context: CallbackContext):
    signal_text = (
        "📈 *سیگنال امروز:*\n"
        "🚀 لانگ: بیت‌کوین در 29,800 دلار\n"
        "📉 شورت: اتریوم در 1,950 دلار\n"
        "🎯 هدف: 3-5 درصد سود\n"
        "⚠️ ضریب پیشنهادی: x3\n"
        "🧠 تحلیل نهنگ‌ها: خرید سنگین بیت‌کوین در صرافی بایننس"
    )
    update.message.reply_text(signal_text, parse_mode="Markdown")

# 🛠️ ساخت و اجرای ربات
def main():
    updater = Updater(TOKEN)
    dispatcher = updater.dispatcher

    # هندلرها
    dispatcher.add_handler(CommandHandler("start", start))
    dispatcher.add_handler(CommandHandler("signal", signal))

    # اجرای ربات
    print("ربات در حال اجراست...")
    updater.start_polling()
    updater.idle()

if __name__ == "__main__":
    main()
