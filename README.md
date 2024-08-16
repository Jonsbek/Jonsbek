  // Node.js Telegram Bot yaratish misoli
                const TelegramBot = require('node-telegram-bot-api');
                
                // Tokenni o'zingiznikiga o'zgartiring
                const token = 'YOUR_TELEGRAM_BOT_TOKEN';
                const bot = new TelegramBot(token, { polling: true });
                
                bot.onText(/\/start/, (msg) => {
                    const chatId = msg.chat.id;
                    bot.sendMessage(chatId, 'Salom! Men sizga yordam bera olishim mumkin.');
                });
                
                bot.onText(/\/help/, (msg) => {
                    const chatId = msg.chat.id;
                    bot.sendMessage(chatId, 'Yordam: Sizga qanday yordam bera olishim mumkin?');
                });
