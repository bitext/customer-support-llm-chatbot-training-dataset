Bitext - Customer Service Tagged Training Dataset for LLM-based Chatbots
========================================================================

Overview
--------

This dataset can be used to train chatbots on Large Language Models such as GPT, Llama2 and Falcon.

The dataset is parallel to our Evaluation dataset (see [Customer Service Tagged Evaluation Dataset for Intent Detection](https://github.com/bitext/customer-support-intent-detection-evaluation-dataset)). Both datasets can be used in conjunction to first train and then evaluate the accuracy provided by training. The main difference between the two datasets is the number of utterances:

  - The training dataset contains 4,514 utterances (around 160 per intent) 
  - The evaluation dataset contains around 270,000 utterances (around 10,000 per intent)

Both datasets share the rest of the specifications, so they can be used in conjunction. The training dataset has the following specs, shared with the evaluation dataset:

  - Customer Service domain 
  - 11 categories or intent groups
  - 27 intents assigned to one of the 11 categories
  - 7 entity/slot types

Each utterance is tagged with entities/slots when applicable. Additionally, each utterance is enriched with tags that indicate the type of language variation that the utterance expresses. Examples include:

  - The tag “COLLOQUIAL” indicates that the utterance contains informal expressions: “can u close my account”
  - The tag “INTERROGATIVE” indicates that the utterance is a question: “how do I open an account”
  - The tag “OFFENSIVE” indicates that the utterance contains offensive expressions: “open my f****** account”

There are a total of 12 tags. See below for a full list of tags, categories and intents.

The purpose of these tags is to customize the dataset so the trained bot can easily adapt to different user language profiles. A bot that sells sneakers and targets a younger population should be proficient in colloquial language; while a classical retail banking bot should be able to handle more formal or polite language.

These intents have been selected from Bitext's collection of 20 domain-specific datasets (banking, retail, utilities...), covering the intents that are common across all 20 domains. For a full list of domains see https://www.bitext.com/chatbot-verticals/.

Utterances and Linguistic Tags
------------------------------------
The dataset contains 4,540 training utterances, with 300 utterances per intent. It has been split into training (80%), validation (10%) and testing (10%) sets, preserving the distribution of intents and linguistic phenomena.

The dataset also reflects commonly occurring linguistic phenomena of real-life chatbots, such as spelling mistakes, run-on words, punctuation errors…

Each entry in the dataset contains the following four fields:

  - context: the domain to which the entry applies
  - role: the role (virtual assistant, user...) that the model should adopt
  - instruction: a user request from the Customer Service domain
  - intent: the intent corresponding to the user instruction
  - entity_type: the type of entity contained in the utterance
  - entity_value: the entity contained in the utterance
  - start_offset: the starting position of the entity
  - end_offset: the ending position of the entity
  - category: the high-level semantic category for the intent
  - tags: different tags that reflect the types of language variations expressed in the utterance
  - response: an example expected response from the chatbot

The dataset contains tags that reflect different language phenomena like colloquial or offensive language. So if an utterance for intent “cancel_order” contains the “COLLOQUIAL” tag, the utterance will express an informal language variation like: “can u cancel my order”

Each utterance is enriched with one or more of these tags:
 - Register tags: colloquial language, polite language…
    - Q - Colloquial variation
    - P - Politeness variation
 - Content tags: offensive language, keyword language…
    - W - Offensive language
    - K - Keyword language
 - Linguistic tags: syntactic and morphological tags (interrogative sentence, coordinated sentence…) 
    - B - Basic syntactic structure
    - C - Coordinated syntactic structure
    - I - Interrogative structure
    - N - negation (don't, can't…)
    - M - Morphological variation (plurals, tenses…)
    - L - Lexical variation (synonyms)
    - E - Expanded abbreviations (I'm -> I am, I'd -> I would…)
 - Real-life errors: spelling errors, punctuation errors…
    - Z - Noise phenomena like spelling or punctuation errors

These tags indicate the type of language variation that the utterance expresses. When associated to each utterance, they allow Conversational Designers to customize training datasets to different user profiles with different uses of language. Through these tags, many different datasets can be created to make the resulting assistant more accurate and robust. A bot that sells sneakers should be mainly targeted to younger population that use a more colloquial language; while a classical retail banking bot should be able to handle more formal or polite language.

You can find more details about the linguistic tags [here](TAGS.md)

Categories and Intents
----------------------
The categories and intents covered by the dataset are:

  - ACCOUNT: create_account, delete_account, edit_account, recover_password, registration_problems, switch_account
  - CANCELLATION_FEE: check_cancellation_fee
  - CONTACT: contact_customer_service, contact_human_agent
  - DELIVERY: delivery_options, delivery_period
  - FEEDBACK: complaint, review
  - INVOICE: check_invoice, get_invoice
  - NEWSLETTER: newsletter_subscription, 
  - ORDER: cancel_order, change_order, place_order, track_order
  - PAYMENT: check_payment_methods, payment_issue
  - REFUND: check_refund_policy, get_refund, track_refund
  - SHIPPING_ADDRESS: change_shipping_address, set_up_shipping_address
  
Entities
--------
The entities covered by the dataset are:

  - account_type
    - Intents: create_account, delete_account, edit_account, switch_account
    - Values: Free, Freemium, Gold, Platinum, Premium, Pro, Standard
  - delivery_city
    - Intent: delivery_options
  - delivery_country
    - Intent: delivery_options
  - invoice_id
    - Intents: check_invoice, get_invoice
  - order_id
    - Intents: cancel_order, change_order, track_order
  - person_name
    - Intents: check_invoice, get_invoice
  - refund_amount
    - Intents: get_refund, track_refund

(c) Bitext Innovations, 2022
