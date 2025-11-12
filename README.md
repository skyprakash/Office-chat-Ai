import random

# 🧠 Predefined responses
responses = {
    "hi": ["Hey boss!", "Hi there 👋", "Hello!"],
    "how are you": ["I'm just a bot, but I’m feeling great!", "Doing awesome, boss 😎"],
    "your name": ["I'm your AI buddy 🤖", "They call me MiniGPT, boss!"],
    "bye": ["Goodbye boss 👋", "See you later!"]
}

def chatbot():
    print("AI Chatbot: Hello boss! Type 'bye' to exit.\n")
    while True:
        user_input = input("You: ").lower()

        if user_input == "bye":
            print("AI Chatbot:", random.choice(responses["bye"]))
            break

        found = False
        for key in responses:
            if key in user_input:
                print("AI Chatbot:", random.choice(responses[key]))
                found = True
                break

        if not found:
            print("AI Chatbot: Hmm, I didn’t quite get that boss 😅\n")

chatbot()
