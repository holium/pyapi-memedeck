To test on MacOS
```bash
mkdir test_memedeck_api && cd test_memedeck_api
python3 -m venv ./venv
source ./venv/bin/activate
python3 -m pip install --index-url https://test.pypi.org/simple/ --no-deps pyapi-memedeck
python3
>>> from pyapi_memedeck import apiclient
```

To use
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
