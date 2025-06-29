# Chatbot
def chatbot_response(user_input):
    user_input = user_input.lower()
    if "hello" in user_input or "hi" in user_input:
        return "Hello! How can I assist you today?"
    elif "return policy" in user_input:
        return "Our return policy allows returns within 30 days of purchase with the original receipt."
    elif "order status" in user_input or "track order" in user_input:
        return "You can track your order using the tracking link sent to your email."
    elif "contact" in user_input or "support" in user_input:
        return "You can contact our support team at support@example.com or call 1800-123-456."
    elif "thank" in user_input:
        return "You're welcome! If you need anything else, feel free to ask."
    elif "bye" in user_input:
        return "Goodbye! Have a great day!"
    else:
        return "I'm sorry, I didn't understand that. Can you please rephrase your question?"
print("Welcome to Customer Service Chatbot!")
while True:
    user_input = input("You: ")
    if user_input.lower() in ["exit", "quit", "bye"]:
        print("Chatbot: Goodbye!")
        break
    response = chatbot_response(user_input)
    print("Chatbot:", response)
