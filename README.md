# Bitext - Customer Service Tagged Training Dataset for LLM-based Virtual Assistants

## Overview

This dataset can be used to train Large Language Models such as GPT, Llama2 and Falcon, both for Fine Tuning and Domain Adaptation.

The dataset has the following specs:

- Use Case: Intent Detection
- Vertical: Customer Service
- 27 intents assigned to 10 categories
- 26872 question/answer pairs, around 1000 per intent
- 30 entity/slot types
- 12 different types of language generation tags

The categories and intents have been selected from Bitext's collection of 20 vertical-specific datasets, covering the intents that are common across all 20 verticals. The verticals are:

- Automotive, Retail Banking, Education, Events & Ticketing, Field Services, Healthcare, Hospitality, Insurance, Legal Services, Manufacturing, Media Streaming, Mortgages & Loans, Moving & Storage, Real Estate/Construction, Restaurant & Bar Chains, Retail/E-commerce, Telecommunications, Travel, Utilities, Wealth Management

For a full list of verticals and its intents see [https://www.bitext.com/chatbot-verticals/](https://www.bitext.com/chatbot-verticals/).

The question/answer pairs have been generated using a hybrid methodology that uses natural texts as source text, NLP technology to extract seeds from these texts, and NLG technology to expand the seed texts. All steps in the process are curated by computational linguists.

## Dataset Token Count

The dataset contains an extensive amount of text data across its 'instruction' and 'response' columns. After processing and tokenizing the dataset, we've identified a total of 3.57 million tokens. This rich set of tokens is essential for training advanced LLMs for AI Conversational, AI Generative, and Question and Answering (Q&A) models.

## Fields of the Dataset

Each entry in the dataset contains the following fields:

- flags: tags (explained below in the Language Generation Tags section)
- instruction: a user request from the Customer Service domain
- category: the high-level semantic category for the intent
- intent: the intent corresponding to the user instruction
- response: an example expected response from the virtual assistant

## Categories and Intents

The categories and intents covered by the dataset are:

- ACCOUNT: create_account, delete_account, edit_account, switch_account
- CANCELLATION_FEE: check_cancellation_fee
- DELIVERY: delivery_options
- FEEDBACK: complaint, review
- INVOICE: check_invoice, get_invoice
- NEWSLETTER: newsletter_subscription
- ORDER: cancel_order, change_order, place_order
- PAYMENT: check_payment_methods, payment_issue
- REFUND: check_refund_policy, track_refund
- SHIPPING_ADDRESS: change_shipping_address, set_up_shipping_address

## Entities

The entities covered by the dataset are:

- {{Order Number}}, typically present in:
- Intents: cancel_order, change_order, change_shipping_address, check_invoice, check_refund_policy, complaint, delivery_options, delivery_period, get_invoice, get_refund, place_order, track_order, track_refund
- {{Invoice Number}}, typically present in:
  - Intents: check_invoice, get_invoice
- {{Online Order Interaction}}, typically present in:
  - Intents: cancel_order, change_order, check_refund_policy, delivery_period, get_refund, review, track_order, track_refund
- {{Online Payment Interaction}}, typically present in:
  - Intents: cancel_order, check_payment_methods
- {{Online Navigation Step}}, typically present in:
  - Intents: complaint, delivery_options
- {{Online Customer Support Channel}}, typically present in:
  - Intents: check_refund_policy, complaint, contact_human_agent, delete_account, delivery_options, edit_account, get_refund, payment_issue, registration_problems, switch_account
- {{Profile}}, typically present in:
  - Intent: switch_account
- {{Profile Type}}, typically present in:
  - Intent: switch_account
- {{Settings}}, typically present in:
  - Intents: cancel_order, change_order, change_shipping_address, check_cancellation_fee, check_invoice, check_payment_methods, contact_human_agent, delete_account, delivery_options, edit_account, get_invoice, newsletter_subscription, payment_issue, place_order, recover_password, registration_problems, set_up_shipping_address, switch_account, track_order, track_refund
- {{Online Company Portal Info}}, typically present in:
  - Intents: cancel_order, edit_account
- {{Date}}, typically present in:
  - Intents: check_invoice, check_refund_policy, get_refund, track_order, track_refund
- {{Date Range}}, typically present in:
  - Intents: check_cancellation_fee, check_invoice, get_invoice
- {{Shipping Cut-off Time}}, typically present in:
  - Intent: delivery_options
- {{Delivery City}}, typically present in:
  - Intent: delivery_options
- {{Delivery Country}}, typically present in:
  - Intents: check_payment_methods, check_refund_policy, delivery_options, review, switch_account
- {{Salutation}}, typically present in:
  - Intents: cancel_order, check_payment_methods, check_refund_policy, create_account, delete_account, delivery_options, get_refund, recover_password, review, set_up_shipping_address, switch_account, track_refund
- {{Client First Name}}, typically present in:
  - Intents: check_invoice, get_invoice
- {{Client Last Name}}, typically present in:
  - Intents: check_invoice, create_account, get_invoice
- {{Customer Support Phone Number}}, typically present in:
  - Intents: change_shipping_address, contact_customer_service, contact_human_agent, payment_issue
- {{Customer Support Email}}, typically present in:
  - Intents: cancel_order, change_shipping_address, check_invoice, check_refund_policy, complaint, contact_customer_service, contact_human_agent, get_invoice, get_refund, newsletter_subscription, payment_issue, recover_password, registration_problems, review, set_up_shipping_address, switch_account
- {{Live Chat Support}}, typically present in:
  - Intents: check_refund_policy, complaint, contact_human_agent, delete_account, delivery_options, edit_account, get_refund, payment_issue, recover_password, registration_problems, review, set_up_shipping_address, switch_account, track_order
- {{Website URL}}, typically present in:
  - Intents: check_payment_methods, check_refund_policy, complaint, contact_customer_service, contact_human_agent, create_account, delete_account, delivery_options, get_refund, newsletter_subscription, payment_issue, place_order, recover_password, registration_problems, review, switch_account
- {{Upgrade Account}}, typically present in:
  - Intents: create_account, edit_account, switch_account
- {{Account Type}}, typically present in:
  - Intents: cancel_order, change_order, change_shipping_address, check_cancellation_fee, check_invoice, check_payment_methods, check_refund_policy, complaint, contact_customer_service, contact_human_agent, create_account, delete_account, delivery_options, delivery_period, edit_account, get_invoice, get_refund, newsletter_subscription, payment_issue, place_order, recover_password, registration_problems, review, set_up_shipping_address, switch_account, track_order, track_refund
- {{Account Category}}, typically present in:
  - Intents: cancel_order, change_order, change_shipping_address, check_cancellation_fee, check_invoice, check_payment_methods, check_refund_policy, complaint, contact_customer_service, contact_human_agent, create_account, delete_account, delivery_options, delivery_period, edit_account, get_invoice, get_refund, newsletter_subscription, payment_issue, place_order, recover_password, registration_problems, review, set_up_shipping_address, switch_account, track_order, track_refund
- {{Account Change}}, typically present in:
  - Intent: switch_account
- {{Program}}, typically present in:
  - Intent: place_order
- {{Refund Amount}}, typically present in:
  - Intent: track_refund
- {{Money Amount}}, typically present in:
  - Intents: check_refund_policy, complaint, get_refund, track_refund
- {{Store Location}}, typically present in:
  - Intents: complaint, delivery_options, place_order

## Language Generation Tags

The dataset contains tags that reflect how language varies/changes across different linguistic phenomena like colloquial or offensive language. So if an utterance for intent “cancel_order” contains the “COLLOQUIAL” tag, the utterance will express an informal language variation like: “can u cancel my order”.

These tags indicate the type of language variation that the entry expresses. When associated to each entry, they allow Conversational Designers to customize training datasets to different user profiles with different uses of language. Through these tags, many different datasets can be created to make the resulting assistant more accurate and robust. A bot that sells sneakers should be mainly targeted to younger population that use a more colloquial language; while a classical retail banking bot should be able to handle more formal or polite language. The dataset also reflects commonly occurring linguistic phenomena of real-life virtual assistant, such as spelling mistakes, run-on words, punctuation errors…

The dataset contains tagging for all relevant linguistic phenomena that can be used to customize the dataset for different user profiles.

### Tags for Lexical variation

M - Morphological variation: inflectional and derivational
“is my SIM card active”, “is my SIM card activated”

L - Semantic variations: synonyms, use of hyphens, compounding…
“what’s my billing date", “what’s my anniversary date”

### Tags for Syntactic structure variation

B - Basic syntactic structure:
“activate my SIM card”, “I need to activate my SIM card”

I - Interrogative structure
“can you activate my SIM card?”, “how do I activate my SIM card?”

C - Coordinated syntactic structure
“I have a new SIM card, what do I need to do to activate it?”

N - Negation
“I do not want this item, where to cancel my order?”

### Tags for language register variations

P - Politeness variation
“could you help me activate my SIM card, please?”

Q - Colloquial variation
“can u activ8 my SIM?”

W - Offensive language
“I want to talk to a f*&%*g agent”

### Tags for stylistic variations

K - Keyword mode
"activate SIM", "new SIM"

E - Use of abbreviations:
“I'm / I am interested in getting a new SIM”

Z - Errors and Typos: spelling issues, wrong punctuation…
“how can i activaet my card”

### Other tags not in use in this Dataset

D - Indirect speech
“ask my agent to activate my SIM card”

G - Regional variations
US English vs UK English: "truck" vs "lorry"
France French vs Canadian French: "tchatter" vs "clavarder"

R - Respect structures - Language-dependent variations
English: "may" vs "can…"
French: "tu" vs "vous..."
Spanish: "tú" vs "usted..."

Y - Code switching
“activer ma SIM card”

---

(c) Bitext Innovations, 2023
