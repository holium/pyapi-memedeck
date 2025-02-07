```python
client = MemeDeckClient(api_key="your_api_key", deck_id="your_deck_id")

# Generate an image
request = GenerateImageRequest(
    prompt="eating ice cream",
    character="pepe",
    aspect_ratio=AspectRatios.SQUARE
)

# Generate and wait for the result
result = client.generate_image(request, wait=True)
print(f"Generated image URL: {result.url}")
```
