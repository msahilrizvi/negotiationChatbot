# negotiationChatbot
This project implements a chatbot that simulates a negotiation process between a customer and a supplier using the **Gemini API** for AI-driven conversation. The chatbot negotiates product prices, accepts counteroffers, or provides discounts based on the user's input.

## Features
- AI-driven negotiation using the **Gemini model**.
- Dynamic conversation: the chatbot responds to the user's offers, either accepting, rejecting, or proposing a counteroffer.
- Flexible user input: customers can choose to accept the bot’s offer, reject it, or propose a counteroffer.
- Realistic negotiation flow: the chatbot will decrement its price gradually if a counteroffer is made, while keeping the price within a predefined range.

## Requirements
- **Python 3.7+**
- **Gemini API** (via LangChain's `ChatGoogleGenerativeAI` integration)

### Python Libraries:
- `langchain-google-genai`
- `langchain-core`
  
### Usage
When you run the script, the chatbot will initiate the negotiation by offering a starting price for a product. The user (customer) can interact with the chatbot in the following ways:
# Accept the bot’s offer: 
  Finalizes the deal at the current price.
# Reject the offer: 
  Ends the negotiation.
# Counteroffer: 
  Propose a new price, and the bot will respond with a negotiation strategy (e.g., accept, reject, or counteroffer based on your input).

### How It Works
# Initial Offer: 
  The bot starts by offering a base price (e.g., $100).
# AI Negotiation: 
  The Gemini model is used to generate dynamic responses during the negotiation process. When the user makes an offer, the chatbot will query the model and   generate a response based on the input.
# Decrementing Price: 
  The bot will gradually reduce its price (within limits) during the negotiation, but will not go below a predefined minimum price.
