import openai

# Replace 'your-api-key' with your actual OpenAI API key
openai.api_key = 'your-api-key'

def generate_serendipity_dream():
    prompt = """
    Generate a serendipity dream, a short whimsical story that blends unexpected luck with surreal and fantastical elements.
    """

    response = openai.Completion.create(
      engine="text-davinci-003",
      prompt=prompt,
      max_tokens=150,
      n=1,
      stop=None,
      temperature=0.7,
    )

    dream = response.choices[0].text.strip()
    return dream

# Example usage
if __name__ == "__main__":
    dream = generate_serendipity_dream()
    print(dream)
