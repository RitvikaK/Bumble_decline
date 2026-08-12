---

# Methodology Summary

The project used a **hybrid analytics approach combining Python-based data processing, NLP techniques, LLM-assisted classification, manual validation, and business analysis**.

This approach allowed large volumes of user feedback to be analysed while preserving the contextual understanding required for product strategy insights.

---

# Methodology

## 1. Data Collection

This project analysed user feedback from multiple sources to identify the key drivers behind Bumble user dissatisfaction and declining engagement.

The final dataset combined:

* Reddit discussions
* Google Play reviews
* App Store reviews
* Kaggle review data

The multi-source approach was used to combine structured customer feedback (app reviews and ratings) with richer qualitative discussions (Reddit).

---

# Reddit Data Collection

Reddit data was collected to capture detailed user experiences, discussions, and complaints surrounding Bumble.

The dataset included:

* Post titles
* Comments
* Subreddit information
* Dates
* Engagement metrics

Initial Reddit data contained general dating discussions alongside Bumble-specific conversations.

To improve relevance, the subreddit **r/Dating_Advice** was removed because a significant proportion of posts focused on general dating advice rather than Bumble-specific product experiences.

The final Reddit dataset focused on discussions directly related to:

* Bumble usage
* Product experience
* Features
* Competitors
* User frustrations

---

# App Review Data Collection

App review data was collected from Google Play and App Store sources.

Collected fields included:

* Review text
* Star rating (where available)
* Date
* Review metadata

An additional Kaggle dataset was incorporated to increase review coverage and provide a broader view of user feedback.

All datasets were standardised and merged into a unified analysis dataset.

---

# 2. Data Preparation

Data preparation involved:

* Combining Reddit, App Store, Google Play, and Kaggle datasets
* Standardising column names and formats
* Cleaning text fields
* Removing irrelevant records
* Preparing datasets for sentiment analysis and categorisation

Separate datasets were maintained where necessary because Reddit discussions and app reviews represent different types of user feedback.

---

# 3. Sentiment Analysis

A hybrid sentiment approach was used depending on the data source.

## App Store & Google Play Reviews

For reviews containing star ratings, sentiment labels were derived from user ratings.

The classification rule was:

| Rating    | Sentiment |
| --------- | --------- |
| 1–2 stars | Negative  |
| 3 stars   | Neutral   |
| 4–5 stars | Positive  |

Ratings were used as the primary sentiment indicator because they provide a direct measure of user satisfaction.

---

## Reddit Discussions

Reddit sentiment required a different approach because discussions do not contain explicit ratings and often rely on conversational context.

An initial VADER sentiment analysis approach was tested; however, this was found to be less reliable for Reddit content due to:

* sarcasm
* short comments
* context-dependent meaning

A more contextual classification approach was therefore applied.

Reddit comments were analysed using both:

* Post title
* Comment text

This allowed classification to consider the wider discussion context rather than treating individual comments as isolated text.

---

# 4. User Theme Classification

Sentiment analysis identifies whether users are positive or negative, but does not explain the underlying reason.

Therefore, a multi-level classification framework was developed to identify the specific drivers behind user sentiment.

Reviews/comments were classified across three levels:

## Dimension

High-level business area:

* Match Quality
* Monetisation
* Trust & Safety
* Product & UX
* Brand & Competition
* Emotional Experience

---

## Category 1

Primary user issue:

Examples:

* Account Issues
* Forced Subscription
* No Matches
* Fake Profiles & Bots
* UX Issues

---

## Category 2

Specific user pain point:

Examples:

* Login & verification failures
* Poor value for money
* Poor support
* Bad quality matches
* Low-effort interactions

---

# 5. Classification Approach

A hybrid human-in-the-loop classification process was used.

## Training Dataset Creation

A subset of reviews was manually labelled to establish:

* category definitions
* examples
* classification rules

This created a reference dataset for scaling categorisation across the wider dataset.

---

## App Review Classification

App Store and Google Play reviews were classified using the original categorisation framework developed from the training dataset.

These reviews were suitable for this approach because they are generally self-contained and structured.

---

## Reddit Reclassification

Due to the contextual nature of Reddit discussions, Reddit data underwent an additional LLM-assisted classification step.

The Anthropic API was used to classify Reddit content using:

* post title
* comment text

The model generated structured outputs including:

* sentiment
* category classification
* confidence

Classification outputs were then reviewed and refined through quality checks.

---

# 6. Quality Assurance

Quality checks were conducted throughout the classification process.

Checks included:

* Reviewing classification consistency
* Identifying incorrect category assignments
* Refining category definitions
* Manually reviewing ambiguous examples

This ensured that automated classification outputs remained aligned with the intended business themes.

---

# 7. Strategic Analysis

The final categorised dataset was analysed using Google Sheets pivot tables and visualisation tools.

Analysis included:

## Sentiment Analysis

Evaluated:

* overall sentiment trends
* sentiment by category
* sentiment by dimension

## Theme Frequency Analysis

Identified:

* most common user complaints
* largest sources of dissatisfaction

## Co-occurrence Analysis

Examined which issues appeared together to uncover deeper relationships between complaints.

Examples:

* Forced Subscription + Poor Value for Money
* Account Issues + Poor Support

## Time-Series Analysis

Analysed changes over time to identify when specific issues increased or decreased.

## Competitive Analysis

Reviews classified under the Brand & Competition dimension were analysed to understand how users compared Bumble with alternatives such as Hinge and Tinder.

---

# 8. Visualisation

Final insights were communicated through:

* Google Sheets pivot tables
* Flourish visualisations
* Strategic presentation slides

Visualisations focused on:

* complaint drivers
* sentiment trends
* category relationships
* strategic recommendations
