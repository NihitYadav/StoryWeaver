# StoryWeaver - AI Story Builder
**StoryWeaver** is an AI-powered storytelling assistant that helps users craft immersive stories, build characters, and generate plots based on prompts or themes. Whether you're a writer, student, or just feeling creative, StoryWeaver can guide you from idea to structured narrative using GenAI.

It uses five core GenAI concepts as described below:

1. System Prompt and User Prompt
--------------------------------
The system prompt defines the assistant’s behavior as a creative story builder. For example:
"You are StoryWeaver, an AI that helps users create imaginative stories based on themes and characters."
The user provides a prompt like: "Write a fantasy story set in ancient Egypt involving a cursed pharaoh."

2. Tuning Parameters
--------------------
The creativity and style of the output are controlled by parameters:
- Temperature: 0.8 (for more creative responses)
- Top_p: 0.95 (to allow a wide choice of vocabulary)
- Max_tokens: 1024 (to ensure full story sections)
- Frequency_penalty: 0.1 (to reduce repetition)

3. Structured Output
---------------------
The output from the AI is formatted as structured JSON-like content, such as:
```
{
  "title": "The Pharaoh's Curse",
  "genre": "Historical Fantasy",
  "characters": [...],
  "setting": "...",
  "plot_summary": "...",
  "twist": "..."
}

```
4. Function Calling
--------------------
StoryWeaver uses function calls for modular content generation:
- generate_character(name, role, genre)
- create_setting(location_type, tone)
- generate_plot_twist(genre)
These help break down story creation into manageable steps and allow AI to build components dynamically.

5. Retrieval-Augmented Generation (RAG)
----------------------------------------
To enhance originality and depth, RAG retrieves external knowledge about themes, myths, or historical events.
For example, for a story involving Norse mythology, the system pulls relevant details about Norse gods or creatures and uses them in the story generation process.