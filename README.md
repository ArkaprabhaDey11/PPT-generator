# PPT-generator
AI PPT Generator: Uses Gemini 2.5 Flash and Pexels API to build decks in seconds. Solved original Overlap Errors by implementing Split-Screen Logic, constraining text to 4.5" to make room for images. Fixed 404 API errors and added 12pt spacing for professional, readable layouts.
# Gemini AI Presentation Generator

An automated PowerPoint generation tool that leverages **Gemini 2.5 Flash** for content research and the **Pexels API** for dynamic image sourcing. This project was specifically designed to solve the "AI Overlap" problem, ensuring professional-grade layouts through programmatic alignment.

## 🚀 The Problem vs. The Solution

### Initial Layout Errors (The "Before")
Early versions of this tool suffered from significant aesthetic issues:
* **Overlap Conflict:** Default PowerPoint text placeholders utilize the full slide width, causing AI-sourced images to sit directly on top of the text.
* **404 Model Errors:** Original attempts to call `gemini-1.5-flash` on outdated API endpoints resulted in "Model Not Found" failures.
* **Cramped Typography:** Text lacked breathing room, crashing into titles and slide borders.

### The Aesthetic Fix (The "After")
The current code implements **Constraint-Based Alignment** to ensure every slide is presentation-ready:
* **Split-Screen Logic:** When an image is present, the script dynamically shrinks the text box width to **4.5 inches**, forcing it to stay on the left half.
* **Vertical Buffering:** A **1.6-inch top margin** prevents body text from colliding with the slide title.
* **Modern Design:** Utilizes a Slate Blue (`44, 62, 80`) and Charcoal palette with **12pt paragraph spacing** for maximum readability.



## ✨ Key Features
* **Automated Research:** Generates a detailed JSON outline based on any topic query.
* **Intelligent Visuals:** Uses Gemini to create descriptive search queries for contextually relevant images.
* **Layout Variety:** Automatically alternates between text-only and split-screen layouts for visual interest.
* **API Stability:** Optimized for **Gemini 2.5 Flash** to ensure high-speed, reliable generation.

## 🛠️ Tech Stack
* **LLM:** Gemini 2.5 Flash
* **Python Library:** `python-pptx` (PPTX manipulation)
* **Image API:** Pexels API
* **Language:** Python 3.10+

## ⚙️ Setup & Installation

1. **Install dependencies:**
   ```bash
   pip install python-pptx google-generativeai requests
2. **Configure API Keys**:

Obtain a Google AI Studio API Key.

Obtain a Pexels API Key.


**USAGE EXAMPLE**: 

```from ppt_generator import PPTGenerator```

# Initialize
generator = PPTGenerator(api_key="YOUR_GEMINI_KEY")

# Generate
```
generator.generate_presentation(
    topic="The Impact of AI in Healthcare", 
    num_slides=6, 
    output_file="AI_Healthcare.pptx"
)
```
**CHANGE LOG**: 

                * Alignment Fix: Constrained text width to 4.5" to eliminate image overlap.

                * Model Migration: Updated to gemini-2.5-flash to resolve 404 connection errors.

                * Styling: Added 12pt paragraph spacing and professional color themes.
