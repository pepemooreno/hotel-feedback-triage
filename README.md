# hotel-feedback-triage

A system that reads customer messages sent to a hotel (reviews, emails and support requests), understands them with an LLM, and turns them into structured data that staff can act on.

> Status: in development. Phase 1 (classification and extraction) is in progress.

## The scenario

The project is built around a fictional hotel, **Hotel Alameda Sur**, an 80-room hotel in Málaga, Spain. All data in this repository is synthetic. No real customer data is used.

Hotels receive messages through many channels and in different styles: formal emails, angry complaints, short reviews, messages with typos, and some in English. Reading and sorting them by hand is slow, and urgent problems can get lost.

## What the system does

For each incoming message, the system extracts:

- **Type:** review, booking inquiry, complaint, special request
- **Topics** (one or more): cleanliness, noise, staff, breakfast, room, location, price, wifi, check-in/check-out, booking and billing
- **Sentiment:** positive, neutral, negative
- **Urgency:** high, medium, low
- **Key data:** booking number, dates, room type, and what the customer is asking for

The output is validated JSON.

## Roadmap

- [ ] Phase 1: classification and extraction with the Claude API, JSON output and a test set
- [ ] Phase 2: draft replies grounded in hotel documents (RAG)
- [ ] Phase 3: routing and an agent that takes actions
- [ ] Phase 4: evaluation and deployment

## Evaluation

A set of messages is labeled by hand and used as ground truth. The goal is to measure how accurate the system is per category, not just to show that it works. Results will be added here as they are available.

## Project structure
