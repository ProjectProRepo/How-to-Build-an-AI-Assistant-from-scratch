# AI Note-Taking Assistant using Transformers

This project builds a lightweight AI-powered assistant that automatically summarizes meeting transcripts using an open-source model from Hugging Face. It is ideal for generating quick meeting notes from long discussions.

## Features

- Reads plain text meeting transcripts
- Summarizes content using a transformer-based model
- Uses Hugging Face's `pipeline` API for simplicity
- Saves the output in a clean, Markdown-formatted summary file
- Runs entirely in Google Colab or locally with minimal setup

## Dependencies

Install the required packages:

```bash
pip install openai-whisper transformers torch accelerate pydub
```

## How It Works

This AI assistant follows a three-step process:

1. **Load the Transcript**: It reads a `.txt` file containing a meeting transcript.
2. **Summarize the Text**: The assistant uses a transformer-based summarization model to condense the content into a brief overview.
3. **Save the Notes**: It generates a Markdown-formatted output file (`meeting_notes.md`) that contains both the summary and the original transcript for reference.

## Hugging Face Login

To access the model used for summarization, you need to log in using your Hugging Face access token. This can be done using the `notebook_login` function from the `huggingface_hub` package.

## Output Format

The output file (`meeting_notes.md`) includes:

- A section titled **Meeting Summary** containing the AI-generated summary.
- A section titled **Full Transcript** that retains the original meeting content.

This format ensures that key points are easy to review, while the full context is preserved for reference.

## Optional Enhancements

- Replace the summarization model with a more advanced open-source LLM such as Mistral, LLaMA, or OpenChat.
- Integrate Whisper to convert meeting audio directly into text before summarization.
- Build a simple interface using Gradio or Streamlit to allow users to upload files and generate notes interactively.
- Add keyword extraction, action item detection, or follow-up task identification using additional NLP pipelines.

## Credits

- Hugging Face Transformers Library  
- Falconsai/text_summarization model on Hugging Face Hub
