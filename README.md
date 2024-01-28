# Project-1
New
pip install chatterbot
pip install chatterbot_corpus
from chatterbot import ChatBot
from chatterbot.trainers import ChatterBotCorpusTrainer

# Create a new chatbot
bot = ChatBot('MyBot')

# Create a new trainer for the chatbot
trainer = ChatterBotCorpusTrainer(bot)

# Train the chatbot on the English language corpus data
trainer.train('chatterbot.corpus.english')

# You can add more training data or customize the bot as needed

# Main loop for interacting with the chatbot
while True:
    user_input = input("You: ")
    
    # Exit the loop if the user types 'exit'
    if user_input.lower() == 'exit':
        break
    
    # Get the bot's response
    bot_response = bot.get_response(user_input)
    
    print("Bot:", bot_response)
